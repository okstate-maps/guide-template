## About
Last Updated *[06/04/2019]*   
Created by [OSU Maps and Spatial Data](https://info.library.okstate.edu/map-room)

![img example](images/OSULogo.png)

## Table of Contents
- Introduction 
- *Georeferencing with ArcPro*
- - Starting a New Project
- - Adding Files
- - Adding Control Points
- - Transforming the Image
- - Deleting Control Points
- - Saving the Project
- Conclusion
- Further Reading/Resources

## Introduction

Georeferencing is the process of adding geographic information to a raster image (i.e. maps, satelite images and aerial photographs) so mapping software can place the image in its real world location. This is done by assigning geographic coordinates to the raster's pixels. 

## McCasland Maps
There are many steps to locating and selecting a McCasland map for georeferencing.
1. Open a web browser and visit the [OSU Library McCasland Maps Collection](https://dc.library.okstate.edu/digital/collection/OKMaps/search/searchterm/McCasland%20Maps/field/collec/mode/exact/conn/and/order/nosort)
2. Browse the maps collection until you find a map with latitude and longitude lines.
3. Click on the map and scroll to the bottom of the page where you will find the file name.

![File Name](images/FileName.PNG)

### Has this map been georeferenced before?
1. To locate this map on the desktop, click **Digitization (\\ulib.okstate.edu)(T:)** aka the *T File*.
2. Click the **Maps** folder.
3. Click **MPSI_Aerials**.
4. Select the **McCasland_Georeferencing** folder and search for the map's file name.
* *Note: If the file name is in this folder, the map has already been georeferenced.

### Locating the File 
1. To locate this map on the desktop, click **Digitization (\\ulib.okstate.edu)(T:)** aka the *T File*.
2. Click the **Maps** folder.
3. Click **Maps_00**.
4. Select the **McCalsand** folder. Here you will see folders sorted by numbers (how to word this).

![Folder Numbers](images/FolderNumbers.PNG)

5. Select the folder that contains the file name of the map you chose and locate to correspondig TIF File.
6. Open the file in *Adobe Photoshop* and click **File, Save As**. 

![Save as JPEG](images/SaveAsJPG.PNG)


7. Make sure to name this new file exactly as the TIF is named and change the *Save as Type* to **JPEG**. Then hit **Save**.

![Save as Type](images/SaveAsType.PNG)

8. A pop up should appear. Do not change any of the settings unless instructed to do so. Click **OK** and exit *Photoshop*.

![JPEG Options](images/JPEGOptions.PNG)

## *Georeferencing with ArcPro*

#### Starting a New Project

1. To begin a new project, open ArcGIS on your desktop.
2. Click **Map** under *New, Blank Templates*.
    
![New Project](images/NewProject.PNG)

3. Name the project and choose a file location that will be easy to access. Then click **OK**. A new screen should open with a map of the world.

#### Adding Files
Now that a new project has been created, a folder connection must be added to import data. 
1. To do this, click **Add Folder** under the *Insert* tab of the toolbar to create a folder connection.

![Folder Connection](images/FolderConnection.PNG)

2. Select the desired folder and click **OK**.
3. The folder connection should appear under *Folders* in the *Catalog* pane. 

![Catalog Connection](images/CatalogConnection.PNG)

4. Locate desired data. Right click the file and click **Add to Current Map**. The selected file is now added to the project and should appear in the *Contents* pane. It is okay if the raster is not displayed on the map as long as the file is visible in the Contents pane.

![Added File](images/AddedFile.PNG)

* *Note: For georeferencing in ArcPro, JPGs are the preferred file type. 

#### Georeferencing

Once a file has been added to the project, the georeferencing process can begin. 

1. In order to start georeferencing, desired file must be selected in the contents pane.
2. Click **Georeference** under the *Imagery* tab of the toolbar. A new *Georeference* tab should appear on the toolbar. 

![Georeference](images/Georeference.PNG)

3. Click **Fit to Display** under the *Georeference* tab. If the raster image was not visible before, it should now appear on the map. The size of the image can be adjusted by zooming in or out and clicking **Fit to Display** as needed. The image does not need to be the exact size of the geographic area it covers. This will be corrected during the georeferencing process.

![Fit to Display](images/FittoDisplay.PNG)

#### Adding Latitude and Longitude
 ##### Adding Control Points
 Control points are used to align pixels on the raster image with real life coordinates. 

 1. To add control points, click **Add Control Points** in the *Adjust* column of the *Georeference* tab.
 
 ![Add Control Points](images/AddControlPoints.PNG)
 
 2. For maps, locate the point of an intersecting latitude and longitude line on the raster image and click. A red box should appear, indicating the selection on the map 
 
 ![Initial Selection](images/InitialSelection.PNG)
 
 3. Turn off the raster layer by clicking the check box next to its name in the *Contents* pane. 
 4. Find the corresponding coordinates on the original world map and click. Be as precise as possible to ensure minimal error. Once this is done, a control point is added. 
 
 ![Control Point](images/ControlPoint.PNG)
 
 6. Continue this step until enough control points are added for the desired transformation. The more control points that are added, the more precise the transformation will be. It is also best to have the control points evenly distributed throughout the map to reduce the chances of a skewed image.   
 
 ![Control Points](images/ControlPoints.PNG)
 
 * *Note: Spline is the preferred transformation for accuracy and requires 10 or more control points, but there are other transformations when this number of control points is not possible.
  
 ##### Transforming the Image
 Transforming the image allows the raster image to be manipulated so the control points overlap.
 
 1. To transform the image, ensure that all necessary control points have been placed. 
 Note: You can add more control points even after the image has been transformed.
 2. Click the **down arrow** under the *Transformation* icon in the adjust section of the georeference tab. Then select the desired transformation.
 
 ![Transformation](images/Transformation.PNG)
 
 * *Note: **Spline** is preffered because it renders the most accurate transformations.
 
 3. The image is now transformed and can be saved or edited if desired.
 
##### Deleting Control Points
Do not fret if a control point is misplaced or results in a skewed image. They are easy to delete!

![Bad Control Point](images/BadControlPoint.PNG)

1. To delete a control point, click **Control Point Table** in the *Review* section of the *Georeference* tab. 

![Control Point Table](images/ControlPointTable.PNG)

2. A table will open at the bottom of the screen. This table shows all of the control point data. If the incorrect control point is unknown, click the checkbox next to a point to uncheck it. If the image becomes unskewed, this is the faulty control point. 

![CP Table](images/CPTable.PNG)

3. To delete a control point, click **Delete** in the *Review* section of the *Georeference* tab. 

![Delete](images/DeleteControlPoint.PNG)

#### Saving the Project
When finished with the project, it is important to ensure that it is saved properly. Clicking the save icon in the top left corner of the screen will not save the georeferenced data. 

There are two ways to ensure a proper save.
-1. Click **Save** in the *Save* section of the *Georeference* tab. This will update the existing raster file that was imported into the project

![Save](images/Save.PNG)

-2. Click **Save as New** in the *Save* section of the *Georeference tab*. This will allow a new and seperate file to be created. The file can be renamed and saved in the desired location.

![Save as New](images/SaveAsNew.PNG)

You can also export the control point data as a seperate file.
1. Click **Export Control Points** in the *Save* section of the *Georeference* tab. This will create a text file with all of the control point data.

![Export Control Point](images/ExportControlPoints.PNG)

2. Name the file and save it in the desired location.

After all of this is done, it is important that the project is closed correctly.
1. Click **Close Georeference** under the *Georeference* tab of the toolbar.

![Close](images/Close.PNG)

The project can be closed and ArcPro can be exited. 

(What about the lat and long lines?)

## Conclusion

## Further Reading/Resources


[Return to Top](#about)
