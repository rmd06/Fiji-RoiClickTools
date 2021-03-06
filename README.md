[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3577888.svg)](https://doi.org/10.5281/zenodo.3577888)

# ImageJ/Fiji Roi 1-Click Tool

<img src="https://github.com/LauLauThom/RoiClicTool/blob/master/Image/FijiMenu.JPG" alt="MenuBar" width="450" height="80">     

Toolset that offers additional toolbar ROI tools, with predefined custom ROI shapes.

Using the 1-Click ROI, clicking on an image generates a predefined ROI, centered on the clicked point.  
If the option are selected, the generated ROI is added to the Roi Manager, the command "run Measure" is run for the selected region and if a stack is used, the next image is displayed. 

## Installation
In Fiji, simply activate the *ROI 1-click tools* update site.  
In ImageJ, copy the file *RoiClicTools.ijm* to the folder *ImageJ\macros\toolsets*. 

## Configuration
Double-click on the ROI icon to configure the shape and options.

<img src="https://github.com/LauLauThom/RoiClicTool/blob/master/Image/Options.JPG" alt="Options" width="300" height="250">

## Video tutorial
[![Tuto](https://img.youtube.com/vi/XeCf2P-jgYM/0.jpg)](https://www.youtube.com/watch?v=XeCf2P-jgYM) 

## Examples
### - Circle tool
Using the 1-click circle tool, one can rapidly measure the average intensity for each dot in the sample image *Dot_Blot*.
<img src="https://github.com/LauLauThom/RoiClicTool/blob/master/Image/DotBlot.png" alt="DotBlot" width="600" height="250">

### - Rectangle tool
Same for the quantification of bands in gels using the 1-click rectangle tool.
<img src="https://github.com/LauLauThom/RoiClicTool/blob/master/Image/Gel.png" alt="Gel" width="650" height="350">

### - Custom macro command
Using the "custom macro command" field, any additional action can be executed upon click.  
Below an example where the clicked region is cropped to a new image using the "duplicate" commands.  
Multiple commands can be entered inline in the one-line field by separating them with ;
<img src="https://github.com/LauLauThom/RoiClicTool/blob/master/Image/customMacro.png" alt="customMacro" width="900" height="320">

### - More complex custom actions
More complex operations can be implemented by adding a few lines in the source code.  
Edit the file `Roi 1-click Tools.ijm` in `Fiji.app/macros/toolsets`. 
Then look for the paragraph

	* MORE CUSTOM COMMANDS (executed even if the tick box is not ticked)
	* Examples (remove the //, save the file and relaunch fiji to test it)
	*/
	//run("Duplicate...", " ");
	//run("Invert", "slice");

You can add some commands of your choice below the examples.

## Credits
If you use those tools please cite  

*Laurent Thomas. (2019, December 16)  
ImageJ/Fiji 1-clic ROI Tool (Version 1)  
Zenodo: http://doi.org/10.5281/zenodo.3577888*
