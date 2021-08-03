# Remote Sensing in QGIS
An introduction to work with remote sensing data in QGIS. <br>
We are using the Semi-Automatic Classification Plugin.


#### Skills needed
- Basics in remote sensing
- Basics in QGIS
  - [What is GIS, and why use QGIS?](https://www.youtube.com/watch?v=8oEnJvLzDnQ) (5 min)
  - [QGIS for Absolute Beginners](https://www.youtube.com/watch?v=kCnNWyl9qSE) (30 min)


#### Technical requirments
- QGIS 3.10 or higher
   - If you need QGIS you can [download QGIS 3.16 Long Term Release here](https://qgis.org/en/site/forusers/download.html) 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="images/QGIS_logo_2017.png" alt="QGIS logo" width="75"><br>
- Account for the [Copernicus Open Access Hub](https://scihub.copernicus.eu/dhus/#/home) 
   - If you need an account you can [register here](https://scihub.copernicus.eu/dhus/#/self-registration) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="images/openhub_service.svg" alt="Copernicus Open Access Hub logo" width="30">

<br>

**Hint:** To ease the installation of the requirements use [*ANACONDA*](https://www.anaconda.com/products/individual). <br>
&nbsp;&nbsp;Create an environment i.e. *rs4gis*, install 
  - python 3.8, 
  - [Numpy](https://anaconda.org/anaconda/numpy), 
  - [SciPy](https://anaconda.org/anaconda/scipy), 
  - [Matplotlib](https://anaconda.org/conda-forge/matplotlib) and 
  - [QGIS](https://anaconda.org/conda-forge/qgis)
 

<br>

---

<br>

## Our goal for today

### Using GIS and Remote Sensing tools to proof why the World Heritage Site [Abu Mena](https://whc.unesco.org/en/list/90) is a in Danger

*Background knowledge:* To be part of the **World Heritage List**, sites must be of **outstanding universal value**.
The List of **World Heritage in Danger** is designed to inform the international community of conditions which **threaten the very characteristics for which a property was inscribed** on the World Heritage List, and to encourage corrective action.
<div align="center">
  <img src="images/Logo-UNESCO-WHL.png" alt="Logo-UNESCO-WHL" width="250">
</div>
 
<br>

#### The steps to achieve our goal
1. Install the  [Semi-Automatic Classification Plugin](https://fromgistors.blogspot.com/p/semi-automatic-classification-plugin.html) for QGIS
2. Download [Sentinel-2](https://sentinel.esa.int/web/sentinel/missions/sentinel-2) data
3. [Preprocess](https://rscc.umn.edu/lessons/lessonpre) the Sentinel-2 data
4. Calculate [NDVI](https://www.dlr.de/eoc/en/desktopdefault.aspx/tabid-9142/19518_read-45426/) & [NDWI](https://foodsecurity-tep.net/node/214)
5. Perform an [image classification](https://gisgeography.com/image-classification-techniques-remote-sensing/)



## What is the Semi-Automatic Classification Plugin?

**The Semi-Automatic Classification Plugin (SCP) is a free open source plugin for QGIS that allows for the supervised classification of remote sensing data and offer functionalities to download, preprocessing and postprocessing of images.**

The overall objective of SCP is to provide a set of functions for raster processing to enable an automatic workflow and ease generation of land cover classifications, especially for beginners of remote sensing methods (Congedo Luca 2020).

<br>


<div align="center">
  <a href="https://www.youtube.com/watch?v=bzynTxwOcYQ&t=65s"><img src="images/SCP_video.PNG" alt="Intro to SCP" width="550"></a>
</div>


<br>

     
<div align="left">

Search and download is available for ASTER, GOES, Landsat, MODIS, Sentinel-1, Sentinel-2, and Sentinel-3 images. Several algorithms are available for the land cover classification. The SCP requires the installation of GDAL, OGR, [Numpy](https://numpy.org/install/), [SciPy](https://www.scipy.org/) and [Matplotlib](https://matplotlib.org/). Some tools i.e. the Random Forest classifier require also the installation of [ESA's SNAP](https://step.esa.int/main/toolboxes/snap/) (Congedo 2020).

 
###### For more detail read:   
*Congedo Luca (2020). Semi-Automatic Classification Plugin Documentation. DOI: http://dx.doi.org/10.13140/RG.2.2.25480.65286/1*

<br>
<br>

---

  
### The steps to achieve our goal
1. Install the  [Semi-Automatic Classification Plugin](https://fromgistors.blogspot.com/p/semi-automatic-classification-plugin.html) for QGIS
2. Download [Sentinel-2](https://sentinel.esa.int/web/sentinel/missions/sentinel-2) data
3. [Preprocess](https://rscc.umn.edu/lessons/lessonpre) the Sentinel-2 data
4. Calculate [NDVI](https://www.dlr.de/eoc/en/desktopdefault.aspx/tabid-9142/19518_read-45426/) & [NDWI](https://foodsecurity-tep.net/node/214)
5. Perform an [image classification](https://gisgeography.com/image-classification-techniques-remote-sensing/)

  
<br>

## 1. Install the Semi-Automatic Classification Plugin (SCP)
<br>
  
Watch this [video](https://www.youtube.com/watch?v=R613_HqT4qo) in a new tab (30 sec) and install the SCP plugin.
  
<div align="center">
  <a href="https://www.youtube.com/watch?v=R613_HqT4qo"><img src="images/scp_screen.PNG" alt="Install SCP" width="750"></a>
</div>

  
<br>
<br>
<br> 
  
## 2. Download Sentinel-2 data

 - After installing the SCP take care that the plugin is activated. &nbsp;&nbsp; <img src="images/plugin_avtivated.PNG" alt="Plugin activated" width="180"><br>
 - Start to open the *Download products* tab of the SCP with &nbsp;&nbsp; <img src="images/download_data.PNG" alt="SCP download button" width="30">
  
> Donwload products &nbsp;&nbsp; <img src="images/scp/scp_download_login-data_button.PNG" alt="SCP download tab login button" width="80">
  
> Login data <br>
> Login Sentinels <br>
> Service: https://scihub.copernicus.eu/apihub <br>
> User & Passwor: Your [personal account](https://scihub.copernicus.eu/dhus/#/self-registration) <br>

- Switch to the *Search* tab & set the search parameters &nbsp;&nbsp; <img src="images/scp/scp_download_search_button.PNG" alt="SCP download tab search button" width="65">
  
    - Select a "*Product*" 
    - Set a "*Date from*"
    - Define "*Max cloud cover*"
    - Set an rectangular area of interest with &nbsp; <img src="images/scp_aoi_button.PNG" alt="SCP aoi button" width="30">
      - left-hand click = upper left corner
      - rigth-hand click = lower rigth corner
 
- Select an appropriate Sentinel-2 scene i.e. the Abu Mena image from 6 April 2021 
  
- Now we click to the "*Download options*" tab &nbsp;&nbsp; <img src="images/scp/scp_download_download-options_button.PNG" alt="SCP download options button" width="110">
  
  - the check boxes of all Sentinel-2 bands need to be activated
  
Watch this [video](https://www.youtube.com/watch?v=R613_HqT4qo) in a new tab (30 sec) and install the SCP plugin.
  
<div align="center">
  <a href="https://www.youtube.com/watch?v=5lN3cajkT0M&t=3s"><img src="images/scp_screen.PNG" alt="SCP download Sentinel-2 data" width="750"></a>
</div>
  
  
  <br>
<br>
<br>
   
   
## 3. Preprocess Sentinel-2 data
- Create a band stack
<br>
  
&nbsp; <img src="images/band_stack.PNG" alt="SCP band stack button" width="30">
  
<br>
<br>
<br> 

###### After preprocessing your data can look like these examples:
<img src="images/s2_tcc-fcc.png" alt="Sentinel-2 true colour composite (left) & false colour composite (rigth)" width="1920">
  
<br>
   
## 4. Calculate NDVI & NDWI
<br>

The **Normalized Difference Vegetation Index (NDVI)** is an indicator of healthy vegetation and thus closely linked to vegetation density and productivity (Tucker & Sellers 1986). The NDVI is calculated using the spectral reflectance measurements of the red and infrared (NIR) wavelength and can range from -1 to +1.

> NDVI = ( NIR – red ) / ( NIR + red )
  
<br>

The **Normalized Difference Water Index** is sensitive to the water content of vegetation and is similar to the NDVI. High NDWI values indicate a high water content of the vegetation. (Gao, B.C., Remote Sensing of the Environment, p.257(1996)). For Sentinel-2 data the NDWI needs Band 8 (NIR) and Band 12 (MIR). 

The NDWI results from the following equation: 
> NDWI = ( NIR - MIR ) / ( NIR + MIR ) 

<br> 
  
&nbsp; <img src="images/band_calc.PNG" alt="SCP band calculator button" width="30">
  
<br> 
<br> 
  
###### After preprocessing your data can look like these examples:
<img src="images/s2_ndvo-ndwi.png" alt="Sentinel-2 NDVI (left) & NDWI (rigth)" width="1920">
  

<br>
<br>

     
More information & tutorials:
- [SCP blog](https://fromgistors.blogspot.com/)
- [SCP youtube channel](https://www.youtube.com/user/fromgistors)

   
<br>
<br>
<br>

  
</div>
