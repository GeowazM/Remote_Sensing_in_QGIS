# Remote Sensing in QGIS
An introduction to work with remote sensing data in QGIS. <br>
We are using the Semi-Automatic Classification Plugin.


#### Skills needed
- Basics in remote sensing
- Basics in QGIS
  - [What is GIS, and why use QGIS?](https://www.youtube.com/watch?v=8oEnJvLzDnQ) (5 min)
  - [QGIS for Absolute Beginners](https://www.youtube.com/watch?v=kCnNWyl9qSE) (30 min)


#### Technical requirments
- Download and install QGIS 2.16 Long Term Release ([Link to download](https://qgis.org/en/site/forusers/download.html)) 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="images/QGIS_logo_2017.png" alt="QGIS logo" width="75"><br>
- Account for the [Copernicus Open Access Hub](https://scihub.copernicus.eu/dhus/#/home) 
   - If you need an account you can [register here](https://scihub.copernicus.eu/dhus/#/self-registration) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <img src="images/openhub_service.svg" alt="Copernicus Open Access Hub logo" width="30">

<br>

---

<br>

## Our goal for today

Using GIS and Remote Sensing to proof why [Abu Mena](https://whc.unesco.org/en/list/90) is a *World Heritage in Danger*

To be part of the World Heritage List, sites must be of outstanding universal value.
The List of World Heritage in Danger is designed to inform the international community of conditions which threaten the very characteristics for which a property was inscribed on the World Heritage List, and to encourage corrective action.


#### The steps to achieve our goal
1. Install the  [Semi-Automatic Classification Plugin](https://fromgistors.blogspot.com/p/semi-automatic-classification-plugin.html) for QGIS
2. Download [Sentinel-2](https://sentinel.esa.int/web/sentinel/missions/sentinel-2) data
3. [Preprocess](https://rscc.umn.edu/lessons/lessonpre) the Sentinel-2 data
4. Calculate [NDVI](https://www.dlr.de/eoc/en/desktopdefault.aspx/tabid-9142/19518_read-45426/) & [NDWI](https://foodsecurity-tep.net/node/214)
5. Perform an [image classification](https://gisgeography.com/image-classification-techniques-remote-sensing/)



## What is the Semi-Automatic Classification Plugin?

**The Semi-Automatic Classification Plugin (SCP) is a free open source plugin for QGIS that allows for the supervised classification of remote sensing images, providing tools for the download, the preprocessing and postprocessing of images (Congedo 2020).**

The overall objective of SCP is to provide a set of intertwined tools for raster processing in order to make an automatic workflow and ease the land cover classification, which could be performed also by people whose main field is not remote sensing (Congedo 2020).

<br>


<div align="center">
  <a href="https://www.youtube.com/watch?v=bzynTxwOcYQ&t=65s"><img src="images/SCP_video.PNG" alt="Intro to SCP" width="750"></a>
</div>


<br>

     
<div align="left">

   Search and download is available for ASTER, GOES, Landsat, MODIS, Sentinel-1, Sentinel-2, and Sentinel-3 images. Several algorithms are available for the land cover classification. This plugin requires the installation of GDAL, OGR, Numpy, SciPy, and Matplotlib. Some tools require also the installation of SNAP (ESA Sentinel Application Platform) (Congedo 2020).

*Congedo Luca (2020). Semi-Automatic Classification Plugin Documentation. DOI: http://dx.doi.org/10.13140/RG.2.2.25480.65286/1*

<br>
<br>

---

<br>

## 1. Install the Semi-Automatic Classification Plugin (SCP)

https://www.youtube.com/watch?v=KkiEdcu5dzs&t=35s
  
<br>
<br>
<br>


## 2. Download Sentinel-2 data


- Sentinel Szene: RT_L1C_T35RQQ_A030234_20210406T085029_B0stack_raster
<br>
<br>
<br>
   
   
## 3. Preprocess Sentinel-2 data
- Create a band stack
<br>
<br>

###### After preprocessing your data can look like these examples:
<img src="images/s2_tcc-fcc.png" alt="Sentinel-2 true colour composite (left) & false colour composite (rigth)" width="1920">
  
<br>
   
## 4. Calculate NDVI & NDWI
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
