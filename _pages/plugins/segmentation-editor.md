---
autogenerated: true
title: Segmentation Editor
categories: Plugins,Segmentation
description: test description
---


{% capture source%}
{% include github org='fiji' repo='VIB' source='Segmentation\_Editor.java' %}
{% endcapture %}
{% include info-box software='ImageJ' name='Segmentation Editor' author='Johannes Schindelin, Francois Kusztos, Benjamin Schmid' maintainer='Benjamin Schmid' filename='VIB\_.jar' source=source status='stable' website='http://132.187.25.13/home/?category=Download&page=SegmentationEditor' %}

Demo video
----------

Segmentation Editor Demo Screencast (5 min 30 sec):

{% include youtube url='https://www.youtube.com/embed/tC-b-BFq6jk'%}

Start
-----

Open the stack containing the structures you want to reconstruct or segment. Go the to the plugins menu and click on "Segmentation Editor". Your stack will be embedded into a segmentation window, and another window opens, which will contain your labels later.

![](/media/Segmentation Editor 1.png "Segmentation_Editor_1.png")

Material
--------

On the left side of the segmentation window, you see a list of available materials. You can extend and modify these materials by right-clicking into the list. For a first start, right-click on Interior, select "Rename" from the popup menu and specify the name of the label you want.

![](/media/Segmentation Editor 2.png "Segmentation_Editor_2.png")

Labelling
---------

Now go through the slices and use ImageJ's selection tools to select the regions you want to label. You don't need to label each slice. When consecutive slices differ only slightly, you can use the built-in interpolation function to label them.

After selecting the regions to label in each slice, click the I-Button (which is next to the Plus and Minus button). This interpolates if you didn't make selections on each slice. Now activate the "3d" checkbox. It means that the selections of all slices will be asigned to a material, not only the selection of the current slice.

![](/media/Segmentation Editor 3.png "Segmentation_Editor_3.png")

Now go to the material list, select the material which you want to asign, and click on the Plus button. That's it.

![](/media/Segmentation Editor 4.png "Segmentation_Editor_4.png")

After finishing, click Ok to close the segmentation window. The labels will remain open. You must store them yourself.

Have also a look at our 3D viewer if you want to see your result in 3D.

![](/media/Segmentation Editor medulla r labels rotating.gif "Segmentation_Editor_medulla_r_labels_rotating.gif")

Starting from a macro
---------------------

The segmentation editor can now be started from a macro, with a user-defined set of materials. Such a macro would look like this:

    // create a new Segmentation Editor
    call("Segmentation_Editor.newSegmentationEditor");

    // Reset the material list
    call("Segmentation_Editor.newMaterials");

    // Add a desired materials
    call("Segmentation_Editor.addMaterial", "MyMaterial1", 255, 255, 0);
    call("Segmentation_Editor.addMaterial", "MyMaterial2", 255, 0, 0);

 