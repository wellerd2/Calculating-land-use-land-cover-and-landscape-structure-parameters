# Calculating-land-use-land-cover-and-landscape-structure-parameters

This code calculates the proportion of each land cover class (cropland, pasture, forest-wetland, shrubland, grassland, barren, open water, developed open space, and developed) as well as impervious cover around each river, lake, pond, or other sampling site using buffers of 122, 366, and 1098. Buffer distances were selected based on Leafy Green Marketing Agreement (https://lgmatech.com/wp-content/uploads/2020/08/CA-LGMA-Metrics-August-2020_Final_Clean_9-18-20.pdf) recommended buffers from the location of any adjacent land uses that are likely to present a food safety risk (Table 7 from Crop Land and Water Sources Adjacent Land Uses). For example, the recommended distance from cropland to a concentrated animal feeding operation (CAFO) with >1,000 head is ~1,200 feet (366 m). We selected this buffer, and buffers 1/3 smaller (122 m) and larger (1,098 m) to obtain land use data. However, **buffer distances can be modified** in the code to meet project needs.

## Overview of Methods:
1. Import sample site shapefiles and csv as well as the National Land Cover Data into R.
2. Confirm all files are in Albers Equal Area; reproject if needed.
3. Recode NLCD data so there is a new file, where the LULC categories are: for.wet, dev.open, dev, pasture, cropland, grass, shrub, open water, and barren cover.
4. Create overlapping buffers around the sampling sites for each of the distance classes listed above which 0 to 122 m, 0 to 366 m, and o to 1,098 m.
5. For each buffer distance determine the total number of pixels within said buffer for each LULC from step [3], and convert this to a percentage.

## Citations
If you download and use a given dataset cite Weller et al (2020) as well as this github (see below).

### GitHub Citation
1. Weller, D. Calculating land use, cover and landscape structure parameters. https://github.com/wellerd2/Calculating-land-use-land-cover-and-landscape-structure-parameters. https://doi.org/10.5281/zenodo.18506634.

### Manuscript Citation
1. Weller, D. L., C. M. Murphy, S. Johnson, H. Green, E. M. Michalenko, T. M. T. Love, and L. K. Strawn. 2022. Land Use, Weather, and Water Quality Factors Associated With Fecal Contamination of Northeastern Streams That Span an Urban-Rural Gradient. Frontiers in Water. Frontiers 0:172.
   

## Papers Used In:
1. Murphy, C. M., D. L. Weller, T. M. T. Love, M. D. Danyluk, and L. K. Strawn. 2025. The probability of detecting host-specific microbial source tracking markers in surface waters was strongly associated with method and season. Microbiol Spectr. https://doi.org/10.1128/spectrum.01972-24
2. Weller, D. L., C. M. Murphy, T. M. T. Love, M. D. Danyluk, and L. K. Strawn. 2024. Methodological differences between studies confound one-size-fits-all approaches to managing surface waterways for food and water safety. Appl Environ Microbiol. https://journals.asm.org/doi/10.1128/aem.01835-23
3. Weller, D. L., T. M. T. Love, D. E. Weller, C. M. Murphy, B. G. Rahm, and M. Wiedmann. 2022. Structural Equation Models Suggest That On-Farm Noncrop Vegetation Removal Is Not Associated with Improved Food Safety Outcomes but Is Linked to Impaired Water Quality. Appl Environ Microbiol. American Society for Microbiology 88.
4. Liao, J., Guo, X., Weller, D.L. et al. Nationwide genomic atlas of soil-dwelling Listeria reveals effects of selection and population ecology on pangenome evolution. Nat Microbiol 6, 1021–1030 (2021). https://doi.org/10.1038/s41564-021-00935-7.
