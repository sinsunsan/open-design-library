# Open library Autocad standard

### Autocad version 

* Save the drawing in autocad 2013 format

### Layers name and content 

#### Ideas behind the normalization choices

We choose to use a limited set of layers named after the way they get printed, and not their physical content. 
Indeed, there is a limited number of print style we use, and at the contrary and very big way to categorize physical content. 
The idea of those starters is have minimal layers that could be used as is, or quickly converted to you autocad style of naming layers

We choose **OL** as a suffix for the library. 
Using a suffix have several advantages : 
* be able to automatically group layers together
* be able to identify layers that come from the library from others...

#### Layers list and content 

All layers are printed in black expect 0L-6 that use layer's colors

* **OL-1-normal** : Normal lines printed (0.15mm) for visible important elements
* **OL-2-thick** : Thick lines printed (0.35mm) for cut elements
* **OL-3-thin** : Thin lines for less important elements visible in the distance.
* **OL-4-dotted** : Dotted thin line printed (0.09mm) for hidden elements
* **OL-5-axis** : Axis style lines
* **OL-6-hatch**: Hatch that get printed using layer's colors
* **OL-7-text**: For text (printed 0.15mm black)
* **OL-8-annotation**: For anotation (printed 0.15mm black)
* **OL-9-guide** : For guides (don't get printed)

### Drawings general settings 

* Drawings need to use the **STB system (Named styles plot styles)**
* Drawings need to be in **centimeters using the metric system**

### Print and drawing areas

* The drawing need to be wrapped in a A4 rectangle at its impression size 
A block is provided for each scale to serve this purpose
* a print settings need to be settle in the paper space using A4 drawings

### Block definition

####  Insertion point 

* Choose the insertion point of the block wisely in a significative point of the object, by default the top bottom, left corner of the object

####  Block and layer

* The objects in the block should be in 0 layer expect if some elements need to be printed with other layers style. For exemple if a block should be placed in layer OL-1-normal instead of settings elements inside this block to OL-1-normal layer, set them at 0 layer so that changing layer will be easy. 

####  Block naming

* name the block in english so that it is descriptive of the element
* use dash "-" separator between words
* suffix the block name by "OL-" that mean Open library and allow to group open library blocks in the list
