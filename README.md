MOST_BIMsurfer
==============

3D BIM Viewer; BIMsurfer extended

authors:
Kaltenriner Christoph (mailchriska@gmail.com) \\
Leichtfried Michael (leichtfried.michael@gmail.com)
TU Vienna

MOST (Monitoring System Toolkit) BIMSurfer 
http://most.bpi.tuwien.ac.at/

###Naming Convention:
- Building Storeys
  All Storeys have to be defined as BuildingStorey Elements. Otherwise the expose and transparent feature will not
  work correctly.
  
- Special Objects (MOST: datapoints)
  Objects of special interest have to begin with dp_; mouse events can be forwarded to external application (eg. GWT)
  
###Fixes:
- special characters in JQuery
   IDs with special characters like the $ sign needs to be escaped. In case of $ in ids, a jquery statement will fail.
- Scrolling to selected Object in Project Tree
   When in 3D View an Object is selected, the Project tree is scrolled to this object
- loading of Projects from BIM Server Repository (thanks to DLabz designlabz@gmail.com,veljko@sigidev.com)
- disappearing objects when panning with touchinput devices
- validated index.html (thanks to Regina Appel regina.appel003@gmail.com)

###Featues:
- Special Objects (Datpoints)
  enhanced features for special objects (defined with dp_)
    - Highlight all special Objects on startup
    - forward mouse events when special objects are selected (no rotate/pan when selected)
    - different highlighting	  
- Toggle Pan and Rotate switch
   A GUI Switch for toggling between Pan and Rotate for use on a Touchscreen or motion control
- Additional Views
   Front, Side and Top Views additional to the Reset View Button
- Zoom-In and Zomm-Out via Sliders
   Zooming via Sliders instead of the mouse wheel to make it usable for Touchscreen and motion control
- Highlight different Objects
   Mark different Objecs from a String Array, as waring object (highlight red)
- Camera movement to a chosen Object (by doubleclicking in Overview Tab)
   Generates two snapshots (from actual position and one from a position with a good view to
   the selected object) and starts the camera movement between these two snapshots
- Transparent 
   Make everything (when nothing is selected) or just a single building storey transparent (by
   selecting anything in this storey) via slider
- Expose
   Expose a storey (by selecting anything in this storey) or expose every storey (when nothing is
   selected)
- Filtering Objects
   Textbox for filtering objectes, which are shown in Filter tab