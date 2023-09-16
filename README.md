# iGEE 

## Summary 
The iGEE web tool, a google earth engine app, was built to facilitate the download of the temperature and landcover datasets for the whole of Australia. iGEE, software as an application (SaaS), provides free and open earth observation datasets on Australian land surface temperature and landcover changes to support SDG research, climate change actions, and governments decision making so that stakeholders can easily assess what is actually happening to Australian cities and communities, starting with data on urban heat islands effect as a priority environmental issue.  

## System architecture 
The diagram illustrates the three-tier architecture of the iGEE web tool. The first tier represents the ‘data acquisition layer’ which accesses the satellite from the GEE catalog and stores the boundary, i.e. the Statistical Area Level or [SA1s](https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs-edition-3/jul2021-jun2026/main-structure-and-greater-capital-city-statistical-areas/statistical-area-level-1) data under GEE cloud assets. The second tier is called the ‘operation layer’, which serves as a logic tier of the web tool. It uses GEE JavaScript libraries to connect the ‘data acquisition layer’ to leverage [Landsat](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2), [Sentinel](https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_S2_SR) and [MODIS](https://developers.google.com/earth-engine/datasets/catalog/MODIS_061_MYD11A2) EO satellite imagery to calculate and export Land Surface Temperature (LST) and Landcover (NDVI & NDBI) parameters for Australia. The third tier represents the ‘iGEE user interface’, which contains the user operation panel and map panel. GEE ui libraries were used to build this layer that connects the backend ‘data acquisition layer’ and ‘operation layer’.

Architecture :

<img width="350" height="600" alt="image" src="https://github.com/IGEE-IHVI/iGEE-app/blob/main/iGEE_system_architecture.png">

## iGEE web tool
Refer to [iGEE web tool](http://www.gisonmeta.com), which represents the third-tier on the GEE platform, built from the ‘data acquisition layer’ and ‘operation layer’ using GEE ui libraries. The web tool interface contains an user operation panel and a map panel. The app calls the specific parameters (land surface temperature or landcover) based on the user’s choice from the user operation panel of the iGEE tool. It then dynamically executes the retrieval algorithm backend and reloads the on-demand results on the map panel. Users need to select a parameter, satellite, time period, data format and a study area to process requests to direct the iGEE tool for computation. Once the computation starts, the tool will display the layers on the right panel. When the computation finishes, the option of ‘ Download result’ will appear on the left panel, which is used for exporting the files to the user’s local drive. Refer to Appendix B for the web tool user manual document. 

Refer to [iGEE web tool user manual](https://github.com/IGEE-IHVI/iGEE-app/blob/main/iGEE%20web%20tool%20user%20manual.pdf) for detailed information on iGEE tool operation. 
<img width="350" height="600" alt="image" src="">

