# Resolved ALMA [C II] 158 μm Observations at Cosmic Noon: Interstellar Medium Structure and Dynamics of the Starbursting QSO SDSS J1000
Codebase for generating figures and results!

Full text is available at: [doi:10.3847/1538-4357/add9a1](dx.doi.org/10.3847/1538-4357/add9a1) (open access) and [arXiv](https://arxiv.org/abs/2504.07325) (even opener access?) and abstract available at [NASA ADS](https://ui.adsabs.harvard.edu/abs/2025ApJ...987...61R/abstract).

## Getting started
You'll have to figure out how to use UV and the included uv.lock file to make a copy of my python environment. It's pretty straightforward I think, I just haven't done it myself...

## Generating most of the plots
Most of the plots in the paper are based on ALMA data. If you want to, you can download the raw data from the ALMA archive to calibrate and image it yourself. But if not (and since that can be a ton of word) I'm including fits files of my reduction and imaging. These files are processed by the notebook in `src/Images.ipynb`. 

## Generating PDR plots
PDR plots are made using PDRTPY. I have a slightly modified version included here. The only customizations I make relative to PDRTPY 2.4.0a are adding a bunch of different ratios to the model set WK2020 (no new lines, just different ratios of existing lines) and a bit of logic in the line ratio plot to allow you to exclude some of the ratios (since I made way too many and only want to use a subset). However, this version of pdrt depends on an older version of astropy that breaks other things in my environment. Luckily UV makes it super easy to make multiple environments. So the pdrt related things are in the pdr_modeling folder and everything else is in src.

## Generating the JWST image
You'll need to download the JWST fits files yourself. See the jwst notebook for hints. Then you should just be able to run it. Make sure to edit the locations of the fits files to match where you downloaded them to. 
