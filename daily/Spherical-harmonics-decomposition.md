# Spherical Harmonics Decomposition

For analyzing [[membrane-fluctuations]] of quasi-spherical [[Giant Unilamellar Vesicle (GUVs)|GUVs]], we decompose the shape into spherical harmonic modes.

## Parameterization

The vesicle surface is described as a small deformation from a sphere:
$$r(\theta,\phi) = R[1 + u(\theta,\phi)]$$

where:
- $R$ = mean radius
- $u(\theta,\phi)$ = dimensionless height field, $|u| \ll 1$
- $(\theta,\phi)$ = spherical coordinates

## Harmonic Expansion

Any function on the sphere can be expanded in spherical harmonics:
$$u(\theta,\phi) = \sum_{\ell=0}^{\infty}\sum_{m=-\ell}^{\ell} u_{\ell m} Y_{\ell m}(\theta,\phi)$$

## Spherical Harmonic Properties

**Orthonormality:**
$$\int Y_{\ell m}^*(\Omega) Y_{\ell' m'}(\Omega) d\Omega = \delta_{\ell\ell'}\delta_{mm'}$$

where $d\Omega = \sin\theta d\theta d\phi$

**Eigenfunction of Laplacian:**
$$\Delta_\Omega Y_{\ell m} = -\ell(\ell+1) Y_{\ell m}$$

This property makes spherical harmonics the natural basis for curvature calculations.

**Reality condition:**
For real $u(\theta,\phi)$:
$$u_{\ell,-m} = (-1)^m u_{\ell m}^*$$

## Mode Interpretation

Each $(\ell, m)$ represents a specific deformation pattern:

**$\ell = 0$:** Spherically symmetric (breathing mode)
- Changes volume
- Eliminated by [[volume-area-constraints]]

**$\ell = 1$:** Translational modes ($m = -1, 0, 1$)
- Shifts center without changing shape
- Set to zero by choosing coordinate origin

**$\ell = 2$:** Quadrupolar deformations
- Ellipsoidal distortions
- First genuine shape mode

**$\ell \geq 2$:** Higher-order shape changes
- Increasing $\ell$ = smaller wavelength features
- More energetically costly ([[bending-rigidity]])

## Geometric Quantities in Harmonic Basis

**Area excess:**
$$\Delta A = \frac{R^2}{2}\sum_{\ell \geq 2, m}[\ell(\ell+1)-2]|u_{\ell m}|^2$$

**Gradient squared:**
$$\int (\nabla_\Omega u)^2 d\Omega = \sum_{\ell,m}\ell(\ell+1)|u_{\ell m}|^2$$

**Parseval identity:**
$$\int u^2 d\Omega = \sum_{\ell,m}|u_{\ell m}|^2$$

## Practical Extraction

From experimental contours $r(\theta,\phi)$:

1. **Compute height field:** $u(\theta,\phi) = \frac{r(\theta,\phi) - R}{R}$
2. **Project onto harmonics:** 
   $$u_{\ell m} = \int u(\theta,\phi) Y_{\ell m}^*(\theta,\phi) d\Omega$$
3. **Compute power spectrum:** $\langle|u_{\ell m}|^2\rangle$
4. **Compare to theory:** [[fluctuation-spectrum-formula]]

## Related
- [[Fourier-analysis]] - 1D analog for periodic boundaries
- [[fluctuation-spectrum-formula]] - what we measure
- [[Helfrich-model]] - energy in terms of harmonics
- [[Einstein summation convention]] - repeated index notation