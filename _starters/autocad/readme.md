# Open library Autocad standard

### Autocad version 

* Save the drawing in autocad 2010 format for backward compatibility (do not use brand new only autocad features with no backward compatibility).

### OL-drawing-block 

This block has 2 functions : 
- serve as a drawing block 
- normalize drawings by importating some definition (layers, text styles) and saved as a dws file be usable to convert layers...


### Layers name and content 

#### Ideas behind the normalization choices

We choose to use a limited set of layers named after the way they get printed, and not by the element they represent. 
Indeed, there is a limited number of print styles we need, and at the contrary a very differents ways to categorize physical content. (think about IFC categorisation process).

The idea of those starters is have minimal layers that could be used as is, or quickly converted to your autocad style of naming layers

We choose **OL** as a suffix for the library. 
Using a suffix have several advantages : 
* be able to automatically group layers together
* be able to distinguish layers that come from the library from others...

#### Layers list and content 

All layers are printed in black expect 0L-6 that use layer's colors

* **OL-1-normal** : Normal lines printed (0.15mm) for visible important elements
* **OL-2-thick** : Thick lines printed (0.35mm) for cutted elements
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

### Paper space, Print and drawing areas

* The drawing need to be wrapped in a A4 rectangle at its impression size 
A block is provided for each scale to serve this purpose
* a print settings need to be settle in the paper space using A4 drawings
* the paper space window need to be locked

### Blocks

### When to use blocks ? 

* Use block always when you have repeated elements in a drawings (for example in a stair the step is reapeated and should use block)
* Use block when you want to group element together to quickly select them despite their are used only one time. 

####  Insertion point 

* Choose the insertion point of the block wisely in a significative point of the object, by default the top bottom, left corner of the object

####  Block and layer

* The objects in the block should be in 0 layer expect if some elements need to be printed with other layers style. For exemple if a block should be placed in layer OL-1-normal instead of settings elements inside this block to OL-1-normal layer, set them at 0 layer so that changing layer will be easy. 

####  Block naming

* name the block in english so that it is descriptive of the element
* use dash "-" separator between words
* suffix the block name by "OL-" that mean Open library and allow to group open library blocks in the list

### Text & annotation 

### Styles 

* Use **open-library** text style and annotation style

#### Text

* Never override text height inside a text or annotation, use global settings of the text object instead (overriding it make it very difficult to reset globally)
* Do not use text but Mtext instead
* Use alway bottom-left alignement (to make it easy place it with insert point)

#### Multi leader

* do not use multi leader, use a simple line + M text instead
* Align text relative to the object to annotate
* Use consistent 45° or orthogonal leader orientation

### Dimension

* Never change properties manually nor override dimension 
* Only play with global factor scale to change text and arrow size "Dim scale overall" under fit section
* Use the same Dim scale overall coef as the text size, for example if you scale the text to 8 model space unit of text height, you should size the dimension to 8 model space units to have the same text size which is a good thing / The arrow and other symbols will automatically scale consistently
*  Use "open-library" dimension style
