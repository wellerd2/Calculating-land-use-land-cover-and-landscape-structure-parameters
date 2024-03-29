# Calculating-land-use-land-cover-and-landscape-structure-parameters

This code calculates the proportion of each land cover class (cropland, pasture, forest-wetland, shrubland, grassland, barren, open water, developed open space, and developed) as well as impervious cover around each river, lake, pond, or other sampling site using buffers of 122, 366, and 1098.  

Overview of Methods:
1. Import sample site shapefiles and csv as well as the National Land Cover Data into R.
1. Confirm all files are in Albers Equal Area; reproject if needed. 
1. Recode NLCD data so there is a new file, where the LULC categories are: for.wet, dev.open, dev, pasture, cropland, grass, shrub, open water, and barren cover.
1. Create overlapping buffers around the sampling sites for each of the distance classes listed above which 0 to 122 m, 0 to 366 m, and o to 1,098 m.
1. For each buffer distance determine the total number of pixels within said buffer for each LULC from [3], and convert this to a percentage.

Bibliography:
1. Liao, J., Guo, X., Weller, D.L. et al. Nationwide genomic atlas of soil-dwelling Listeria reveals effects of selection and population ecology on pangenome evolution. Nat Microbiol 6, 1021–1030 (2021). https://doi.org/10.1038/s41564-021-00935-7.

Papers Used In:
1. Liao, J., Guo, X., Weller, D.L. et al. Nationwide genomic atlas of soil-dwelling Listeria reveals effects of selection and population ecology on pangenome evolution. Nat Microbiol 6, 1021–1030 (2021). https://doi.org/10.1038/s41564-021-00935-7.

