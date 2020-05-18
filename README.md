# Exercise: Mapping Educational Attainment in New York

### Summary

This exercise is an introduction to QGIS. It focuses on mapping 
educational attainment data for New York State.

### Input Data

There are two input files on the Google drive for the course: 
**tl_2016_us_county.zip**, a shapefile giving the boundaries of New York 
counties, and **attainment.csv**, a file containing data from the Census 
about educational attainment for New York counties. Variables in the 
attainment file with prefix `'pct_'` give the percentage of the 
population having educational attainment in one of five categories: 
less than high school (`<hs`); high school or GED (`hs`); some college 
or an associate's degree (`some_col`); a bachelor's degree (`ba`); or a 
graduate or professional degreee (`grad`). The ratio variable gives 
the ratio of people with a BA or more (`ba` and `grad`) to those 
with a high school diploma or less (`<hs` and `hs`). 

### Deliverables

One QGIS project file called **attain.gqz** and two PNG images: one called
**below_hs.png** that is a heat map of the `'pct_<hs'` variable in 
`attainment.csv`, and another called **ratio.png** that is a heat map of 
the `'ratio'` variable. 

### Instructions

1. Start a new project in QGIS.

1. Add the layer with country boundaries.

1. Use Save As to save the project in the GitHub directory for the 
assignment under the name `'attain'`. The extension `'.gqz'` will 
be added automatically (if you're using an older version of QGIS it 
may be different). Be sure the file ends up in the directory for the 
assignment so it will be pushed correctly. 

1. Add county name labels and turn on the text buffer around the name.

1. Add the `'attainment.csv'` file.

1. Join `'attainment.csv'` onto the county layer using `'geoid'` as the 
join key and `'at_'` as the variable prefix.

1. Construct the heat map for `'at_pct_<hs'` using equal intervals and 5 
classes. You can use any color scheme you like.

1. Save the project again.

1. Export the map as **below_hs.png** and save it in the directory 
for the assignment.

1. Change the heat map to show `'at_ratio'`. Use pretty breaks and
5 classes. You can use any color scheme you like.

1. Export the new map as **ratio.png** to the directory for the assignment.

### Submitting

Once you're happy with everything and have committed all of the changes to
your local repository, please push the changes to GitHub. At that point, 
you're done: you have submitted your answer.

### Tips

+ If you want, you can create the second map by right-clicking on the first
county layer, selecting 'Duplicate Layer', and then editing the new layer
to match the second set of specifications. If you do that, you should 
rename the duplicated layer to something more meaningful than the original
name with "copy" added. Right click on the name and look for the Rename 
Layer option. Once you've created the new layer you can switch back and 
forth between them by clicking on the check box next to the layer name 
in the Layers Panel.
