# stacks_C3emittersVANDELS
This repository contains the spectra used for the analysis of CIII] emitters in VANDELS presented in Llerena et al. 2021

We made median stacking with a sample of 217 galaxies splitting it by ranges of mass (5 bins) and also ranges of Ks magnitude (6 bins) and FUV (1500A) magnitude (6 bins), from BAGPIPES SED fitting.  We also have stacks by equivalent width (EW) of LyA (4 bins) and CIII] (3 bins)

There are 5 folders: M_1500, Stellar mass, and Ks_VISTA,  EWLyA and EWCIII] depending on the parameter. 

Inside each folder, there are 4 subfolders (StackA, StackB, StackC, StackD) depending on the galaxies included in the stacks. 
“StackA” : all galaxies in the bin are included in the stack. 
“StackB”: only galaxies with Lya in the spectral range in the bin are included (galaxies at z>2.93) 
“StackC”: only galaxies with EW(LyA)>0 in the bin are included (galaxies at z>2.93) 
“StackD”: only galaxies without Lya in the spectral range in the bin are included (galaxies at z<=2.93)
In some cases, where there were less than 4 galaxies per bin after this redshift classification, some of the original bins were combined to ensure a good S/N. 

For the stacking by EW(LyA) just the galaxies with LyA measurements (from https://arxiv.org/pdf/2001.11063.pdf ) were included and there is just one kind of stack for this parameter (equivalent to StackB). 

Every spectra are normalized to the average continuum flux at ~1500A. 

Each file has two extensions: ‘PRIMARY’ (the stacked spectrum) and ‘ext 1’ (the corresponding error spectrum).

Format of the file name: 
'stack(stack number)-(parameter)-Stack(kind of stack)-rebin.fits', where: 

“stack number”: this can go from 1 to 6 
“parameter”: this can be 'mass' (for mass), ‘MFUV’ (for FUV magnitude), ’MKs’ (for Ks magnitude), EWLyA (for EW(Lya)), EWC3 (for EW(CIII]))
“kind of stack”: this can be ‘A’, ‘B’, 'C', or ‘D’
