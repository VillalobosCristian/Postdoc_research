---
title: Fluctuation spectroscopy of giant unilamellar vesicles using confocal and phase contrast microscopy
authors: Hammad A. Faizi, Cody J. Reeves, Vasil N. Georgiev, Petia M. Vlahovska, Rumiana Dimova
year: 2020
citekey: faizi2020
tags: [paper]
aliases: [faizi2020]
DOI: 10.1039/D0SM00943A  
URL: 
---
# Fluctuation spectroscopy of giant unilamellar vesicles using confocal and phase contrast microscopy

**Authors:** Hammad A. Faizi, Cody J. Reeves, Vasil N. Georgiev, Petia M. Vlahovska, Rumiana Dimova  
**Year:** 2020  
**Journal:** Soft Matter

## Summary
Compares [[confocal-microscopy]] vs [[phase-contrast-microscopy]] for measuring [[bending-rigidity]] of [[GUVs]] using [[../projects/GUVs/Fluctuation-spectroscopy-derivation]]. Both methods give consistent results when done correctly.

## Key Points
- [[../projects/GUVs/Fluctuation-spectroscopy-derivation]] (flickering analysis) measures [[membrane-fluctuations]] to determine [[bending-rigidity]]
- Vesicle contour is analyzed using [[Fourier-analysis]] 
- Both confocal and phase contrast work if: proper focus, avoid drift, correct for optical artifacts
- Common errors: wrong focal plane, sample drift, improper background subtraction

## My Notes
Important for my GUV work - I should use fluctuation analysis to measure membrane properties before/after optothermal heating.

Need to implement proper [[contour-detection]] in my analysis pipeline.

## Relevance to My Work
Could combine [[../projects/GUVs/Fluctuation-spectroscopy-derivation]] with [[optothermal-heating]] to study how temperature affects [[membrane-mechanics]].

Related to my [[MSCA-2025]] proposal - measuring membrane properties.

## Related Concepts
- [[bending-rigidity]]
- [[../projects/GUVs/Fluctuation-spectroscopy-derivation]]
- [[GUVs]]
- [[membrane-fluctuations]]
- [[Helfrich-model]]

## Related Papers
## Theoretical Foundation
This paper implements the quasi-spherical fluctuation spectrum derived from [[Helfrich-model]]:
$$\langle |u_{\ell m}|^2\rangle = \frac{k_BT}{\kappa[\ell(\ell+1)-2][\ell(\ell+1)+\sigma R^2/\kappa]}$$

Key implementation details:
- Need proper [[contour-detection]] to extract $u(\theta,\phi)$
- [[Fourier-analysis]] → spherical harmonics decomposition
- [[volume-area-constraints]] eliminate $\ell=0,1$ modes

See full derivation in [[../projects/GUVs/fluctuation-theory-derivation]]