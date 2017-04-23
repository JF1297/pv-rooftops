
Hypotheses:
* The probability of solar cells being installed in a given location is directly affected by the amount of sunlight the location receives per day 
* The amount of sunlight a given location receives per day is directly affected by the amount of tree canopy over the location


Hypothesis:
* Combining the above two:  The probability of solar cells being installed in a given location is directly affected by the percent tree canopy over that location.


Step 1:  Need to find a quality source of tree canopy data for the United States.

Progress:

* Downloaded 2011 US Forest Service Tree Canopy 2011 Edition
* https://catalog.data.gov/dataset/national-land-cover-database-nlcd-percent-tree-canopy-collection
* Description (from above website):
-- "NLCD 2001 Percent Tree Canopy was developed in three key steps: 1. Reference data of tree canopy density was derived from the high spatial resolution images. 2. Density prediction models were calibrated using reference data and Landsat spectral bands. 3. The models developed in step 2 were extrapolated spatially to map per-pixel tree canopy density. This method is described in detail in Huang et al. (2001). NLCD 2011 Percent Tree Canopy Cartographic is the cartographic version of the NLCD 2011 Percent Tree Canopy Analytical dataset for the 48 conterminous states. It was produced by the USDA Forest Service Remote Sensing Applications Center (RSAC). Tree canopy values range from 0 to 100 percent. The analytic tree canopy layer was produced using a Random Forests regression algorithm. The cartographic product is a filtered version of the regression algorithm output."


* After un-zipping, the dataset is 17+ GB
* Description (from the included html file in the zipped folder):  the National Land Cover Database 2011 (NLCD2011) USFS percent tree canopy product was produced with the primary goal of generating current, consistent, and seamless national land cover, percent tree canopy, and percent impervious coer at medium spatial resolution.  Tree canopy values range from 0 to 100 percent.  The analytic tree canopy layer was produced using a Random forests regression algorithm.
* Description (From readme): "The TCC 2011 dataset has two layers:  percent tree canopy cover and standard error. For layer one, the percent tree canopy cover layer, the pixel values range from 0 to 100 percent and represent the percent of the ground covered by a vertical projection of tree canopies. For layer two, the standard error layer, the pixel values range from 0 to 45 percent. The standard error represents the model uncertainty associated with the corresponding pixel in the tree canopy cover layer. The percent tree canopy cover layer was produced using a Random Forests (trademarked by Leo Breiman and Adele Cutler) regression algorithm and the standard error layer was calculated from the variance of the canopy cover estimates from the random forest regression trees."





Next:

*2016 Research Paper: Riemann et al., "Comparative assessment of methods for estimating tree canopy cover across a rural-to-urban gradient in the mid-Atlantic region of the USA"
*https://www.fs.fed.us/nrs/pubs/jrnl/2016/nrs_2016_riemann_001.pdf
*Study compared four different methods: "The first two, field-collected and photointerpreted, are currently acquired by FIA on approximately 44,000 plots annually nationwide.  The third method is a stem-mapping approach that models tree canopy cover from variables regualrly measured on forested plots and is efficient enough to calculate nationwide.  The fourth is a Geographic-Object-Based Image Analysis (GEOBIA) approach that uses both high-resolution imagery and leaf-off LiDAR data and has reported very high accuracies and spatial detail at state-wide levels of application....Plot-and county-level estimates of tree canopy cover derives from each of the four data sources were compared for 11 counties in Maryland, Pennsylvania, and West Virginia across a range of urbanization levels."
*
