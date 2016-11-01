# Ignore these notes 

## Notes

- The data/structures were collated from filtering files on slapper /u24/Experiments (not /u24/local/svnrepos), so I will need to double check the sources to give credit, and have the right experimental parameters. Most are from Xiaohao, so confirmation is an e-mail away. 

- 1P and 2P fits (Wurzite +/- Zinc Blende) to the "whitelight" NP dataset have been done, in segmented DDPs set up as solution sets, to guide the reader through the CdSeNP "story" (ie. how the turbostratic disorder was uncovered, and how mixed phase stacking fault models were made). Fits are under `data/mixedPhase_NPandBulk_whiteLight/fitBase`. The refinements show good agreement to XY's mixed phase modelling in SrFit and published results, importantly, the stacking fault densities from the low-R regions ("three-layers") are consistent. Some of the SrFit contstraints, namely the NN bond dist. in R, and the Wurzite:ZincBlende P1 UC volumes, can't be done in PDFgui (I don't think). But, the results from the gui refinements mostly satisfy these constraints. We can confirm validity together if necessary, but there is a chance the 2P fits are outside the scope of the 1st chapter; I have chosed to add them here, in case we want to complete the story for our readers.   

## Concerns: More important 

- Do not have a Ni measurement for the NP series collected at MUCAT
- We can pull Qdamp from XY's param dict. in his srfit recipe. XY fixed Qdamp to this value in all refinements, and does not refine Qdamp. **Edit**: It is clear now that Qdamp was obtained from the full-range single-phase Wurzite refinement to CdSe bulk. I believe this is kosher.   

```python
    p0=dict(
        {'cdse_wur_a':      4.299,
         'cdse_wur_c':      7.01,
         'cdse_zin_a':      6.00,
         'cdse_zin_b':      6.112,
         'cdse_zin_c':      6.111,
         'z_cdse_wur':      0.3758,
         'cd_uiso':         0.017,
         'se_uiso':         0.02,
         'delta2_cdse_wur': 6.184,
         'delta2_cdse_zin': 5.918,
         'delta_z':         0.0400389,
         'firstbond':       2.6048,
         'firstbond_zin':   2.6048,
         'scale':           0.059,
         'scale_wur':       0.60,
         'thetafb':         0.3609,
         'thetafb1':        0.61575,
         'thetafb2':        0.7854,
         'qdamp':           0.058,

         })
```

- My default/easiest choice for the CdSe dataset to be used for the 2nd "diffpy-dscreteNP" chapter would be `fitCdSeNP` from cmi-exchange. I am including it here, but will relocate once things are more concrete. If there is consensus, and we choose to give the full stacking fault story, I would also like to provide both PDFgui and SrFit solutions to the mixed phase models somehere. I think that could be helpful. 

### Concerns: Less important

##### Under ../structures/cif

- Do not know what `cdo_XY.cif` triclinic structure with a=b=c is. Guessing some cadmium oxide impurity phase?
- All `..XY.cif` have the SG symm. removed. 

##### Under ../structures/stru

- Don't know what the `sf.stru` model is, with greatly elongated C-axis. 

##### Under /data/SCXRD_NP_gramScale

- Collecting this set, for backup, or in case useful for 2nd NP chapter
- Missing PDF data files for: CdSe350; CdSe380
- Found: CdSe408