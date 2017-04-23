
Hypotheses:
* The probability of solar cells being installed in a given location is directly affected by the amount of sunlight the location receives per day 
* The amount of sunlight a given location receives per day is directly affected by the amount of tree canopy over the location


Hypothesis:
* Combining the above two:  The probability of solar cells being installed in a given location is directly affected by the percent tree canopy over that location.
* i.e. If your roof is covered in shade (due to nearby trees or tall buildings) most of the day throughout the year, it might not have a favorable enough “solar window” to justify the costs of solar panel installation. 


more info 
* http://news.energysage.com/installing-home-solar-panels-with-a-hoa/
* http://www.itreetools.org/
* https://landscape.itreetools.org/maps/locations/
* https://www.loc.gov/preservation/digital/formats/fdd/fdd000420.shtml
* The format we are calling ERDAS_IMG to distinguish from other uses of the .img file extension is a proprietary, partially documented format for multi-layer geo-referenced raster images developed originally for use with ERDAS IMAGINE software. This format is used widely for processing remote sensing data, since it provides a framework for integrating sensor data and imagery from many sources. This description covers all chronological versions of the format because the compilers of this resource have been unable to find documentation that clearly distinguishes between formats as produced by different versions of the software. Comments welcome. This format is one of the formats used for data delivery via the National Map as of early 2015, in particular for the National Elevation Dataset (NED).
* Viewing the ERDAS_IMG multi-layered images requires specialized software.
There appear to be two software libraries that support the reading and writing of ERDAS_IMG files:
* The open source GDAL/OGR library. See GDAL: HFA -- Erdas Imagine .img. This capability in GDAL derives from a project evidently supported by Intergraph around 2004. Intergraph was owner of ERDAS IMAGINE software at the time. This project yielded a C++ API that is integrated into GDAL and also a utility img2tif designed to convert ERDAS_IMG files to GeoTIFFs. As of January 2015, the former link to the source code for img2tif (with a date of 2006) is no longer online. See former project page via the Internet Archive for more information. The compilers of this resource do not know whether GDAL support handles new variants of the ERDAS_IMG format. Comments welcome. This library is used by the open source QGIS and GRASS applications.
* The IMAGINE Developers' Toolkit, included in the Producer suite of the Power Portfolio from Hexagon Geospatial. This toolkit supports reading and writing of ERDAS_IMG files.

* https://databasin.org/maps/new#datasets=ff946d025fb0487184d498027a4ce205
* https://www.arcgis.com/home/webmap/viewer.html?webmap=2fd891eae0e94c0d8a5d12dbeff1e1ea


Step 1:  Need to find a quality source of tree canopy data for the United States.

Progress:

* Downloaded 2011 US Forest Service Tree Canopy 2011 Edition
* https://catalog.data.gov/dataset/national-land-cover-database-nlcd-percent-tree-canopy-collection
* Description (from above website):
-- "NLCD 2001 Percent Tree Canopy was developed in three key steps: 1. Reference data of tree canopy density was derived from the high spatial resolution images. 2. Density prediction models were calibrated using reference data and Landsat spectral bands. 3. The models developed in step 2 were extrapolated spatially to map per-pixel tree canopy density. This method is described in detail in Huang et al. (2001). NLCD 2011 Percent Tree Canopy Cartographic is the cartographic version of the NLCD 2011 Percent Tree Canopy Analytical dataset for the 48 conterminous states. It was produced by the USDA Forest Service Remote Sensing Applications Center (RSAC). Tree canopy values range from 0 to 100 percent. The analytic tree canopy layer was produced using a Random Forests regression algorithm. The cartographic product is a filtered version of the regression algorithm output."

https://www.mrlc.gov/nlcd11_data.php

NLCD 2011 USFS Tree Canopy cartographic (3.2 GB)
The U.S. Forest Service cartographic canopy product is designed for the standard user who requires the single best representation of tree canopy designed for most applications. This product consists of a single layer, percent tree canopy cover, with file pixel values ranging from 0 to 100 percent, with each individual value representing the area or proportion of that 30m cell covered by tree canopy. The product is then filtered and masked to eliminate obvious non-tree areas, and to create a more cartographically useful product. Although this approach more closely resembles the NLCD 2001 tree canopy protocol, the products still used different mapping methods and are not designed to be directly comparable for change analysis. The percent tree canopy cover layer was produced using a Random Forests (trademarked by Leo Breiman and Adele Cutler) regression algorithm. 


NLCD 2011 USFS Tree Canopy analytical (10.4 GB)
The U.S. Forest Service analytical canopy product is designed for users that require more analytical vigor in their applications. This product has two layers: percent tree canopy cover (layer one) and standard error (layer two). For layer one, the percent tree canopy cover layer, the file pixel values range from 0 to 100 percent, with each individual value representing the area or proportion of that 30m cell covered by tree canopy. No masking of obvious non-tree areas is performed for this product. For layer two, the standard error layer, the file pixel values range from 0 to 45 percent, with each individual value representing the standard error for the model in that 30m cell. The higher the value, the greater the model uncertainty in estimating the canopy value for that cell. The percent tree canopy cover layer was produced using a Random Forests (trademarked by Leo Breiman and Adele Cutler) regression algorithm and the standard error layer was calculated from the variance of the canopy cover estimates from the random forest regression trees. This mapping methodology is different from the previous NLCD 2001 canopy product, which results in a current product that is not designed to be comparable to NLCD 2001 canopy for change detection. 






* After un-zipping, the dataset is 17+ GB
* Description (from the included html file in the zipped folder):  the National Land Cover Database 2011 (NLCD2011) USFS percent tree canopy product was produced with the primary goal of generating current, consistent, and seamless national land cover, percent tree canopy, and percent impervious coer at medium spatial resolution.  Tree canopy values range from 0 to 100 percent.  The analytic tree canopy layer was produced using a Random forests regression algorithm.
* Description (From readme): "The TCC 2011 dataset has two layers:  percent tree canopy cover and standard error. For layer one, the percent tree canopy cover layer, the pixel values range from 0 to 100 percent and represent the percent of the ground covered by a vertical projection of tree canopies. For layer two, the standard error layer, the pixel values range from 0 to 45 percent. The standard error represents the model uncertainty associated with the corresponding pixel in the tree canopy cover layer. The percent tree canopy cover layer was produced using a Random Forests (trademarked by Leo Breiman and Adele Cutler) regression algorithm and the standard error layer was calculated from the variance of the canopy cover estimates from the random forest regression trees."





Next:

*2016 Research Paper: Riemann et al., "Comparative assessment of methods for estimating tree canopy cover across a rural-to-urban gradient in the mid-Atlantic region of the USA"
*https://www.fs.fed.us/nrs/pubs/jrnl/2016/nrs_2016_riemann_001.pdf
*Study compared four different methods: "The first two, field-collected and photointerpreted, are currently acquired by FIA on approximately 44,000 plots annually nationwide.  The third method is a stem-mapping approach that models tree canopy cover from variables regualrly measured on forested plots and is efficient enough to calculate nationwide.  The fourth is a Geographic-Object-Based Image Analysis (GEOBIA) approach that uses both high-resolution imagery and leaf-off LiDAR data and has reported very high accuracies and spatial detail at state-wide levels of application....Plot-and county-level estimates of tree canopy cover derives from each of the four data sources were compared for 11 counties in Maryland, Pennsylvania, and West Virginia across a range of urbanization levels."
*
