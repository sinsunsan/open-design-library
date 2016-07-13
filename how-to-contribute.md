
# Drawings rules to follow

To the open library a consistent quality, we need to decide good ways of drawings and exclude others. 
That does not mean your habits are bad, but to enforce reusability we need standardisation !

# AUTOCAD rules to contributes to the open library

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

* OL-1-normal : Normal lines printed (0.15mm) for visible important elements
* OL-2-thick : Thick lines printed (0.35mm) for cut elements
* OL-3-thin : Thin lines for less important elements visible in the distance.
* OL-4-dotted : Dotted thin line printed (0.09mm) for hidden elements
* OL-5-axis : Axis style lines
* OL-6-hatch: Hatch that get printed using layer's colors
* OL-7-text: For text (printed 0.15mm black)
* OL-8-annotation: For anotation (printed 0.15mm black)
* OL-9-guide : For guides (don't get printed)

### Drawings general settings 

* Drawings need to use the STB system (Named styles)
* Drawings need to be in centimeter using the metric system

### Print and drawing areas

* The drawing need to be wrapped in a A4 rectangle at its impression size 
A block is provided for each scale to serve this purpose
* a print settings need to be settle in the paper space using A4 drawings
