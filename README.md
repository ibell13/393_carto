# Cartography Portfolio
> Isaac Bell

> ibell2@uoregon.edu

***

### *Cartographer's Statement*
I am a fourth-year student at the University of Oregon studying spatial data science. I'm particularly interested in using remote sensing
and GIS to explore natural science. I am building my cartography skills in order to tell engaging stories about the earth, and to present any of my future 
work in a visually pleasing way. This portfolio is a collection of work from Geography 393, Data Driven Cartography; all of it was created in ArcGIS Pro.
***

## Lab 1: Reference maps at three scales
![Layout_lab1-1](https://github.com/ibell13/393_carto/assets/122644517/75aa0cf6-e629-456e-a07d-527e7c736c91)
[PDF Version](./pdfs/Layout_lab1.pdf)

In my first project, I created three reference maps: one small-scale map of the Willamette Valley, and two larger-scale maps of Portland, OR and Salem, OR.
All of these maps were required to show roads, cities, states, counties and water bodies, but with varied symbology and labeling across each map; I also chose to add several
additional features to some maps, such as land use and local points of interest. 

For my map of the Willamette Valley, I decided to use layers that
emphasized larger geographic features and patterns. I used OpenStreetMap's land use data to emphasize land cover patterns across the valley; I also emphasized political
features like counties and large cities. One way I varied my symbology between feature
types was using serif fonts for state and county labels, and sans serif for cities and
towns.

For my map of Portland, the scale seemed best for labeling neighborhoods. I
used the OpenStreetMap 'places' dataset for this. My main
goal for this map was to keep a simple and consistent color scheme.

For my map of Salem, I chose to de-emphasize roads and focus on buildings and
points of interest in the city. For this, I used the OSM 'parks & squares' dataset, with a
definition query selecting parks, schools, universities, "attractions" and libraries. I then
labeled these features, giving attractions and universities a larger font size than the
other categories (and not labeling parks at all). I also used the OSM 'buildings' dataset.

For all three maps, I tried my best to avoid cluttering the map with unnecessary
data and labels, but it was difficult to balance information and aesthetics. Using different color schemes at every scale may have made the results look disjointed, but
I feel like it makes the differences between each map clearer.

## Lab 2: Choropleth maps across space and scale
![Layout_lab2-1](https://github.com/ibell13/393_carto/assets/122644517/b3e15212-216d-4320-8bb2-2f2ba6531c0d)
[PDF Version](/pdfs/Layout_lab2.pdf)

In my second project, I used census data to create a diverging color choropleth map with consistent data classification at the county and census tract level.
Starting with raw 2020 census tables of population characteristics, I created a new column that calculated the percent of people born in a given state out of the total
population. I then binned this data into user-defined classes based on its distribution, a graph of which is shown below:
![Screenshot 2023-12-06 181519](https://github.com/ibell13/393_carto/assets/122644517/977a6698-a096-44c1-ac32-9cbf1bac276d)

For my maps, I chose to use a custom classification scheme with 7 classes. I
was most interested in showing deviation from the average in-state born percentage, so
I set the critical break (at 65-70%) close to the county-level data's mean and median (67% and 70%,
respectively). Other parts of the data that I wanted to show were the extremely high or
low values. To do this, I adjusted the highest (over 84%) and lowest (less than 40%)
bins to each have around 200 data points, less than any of the other classes.
Otherwise, I attempted to strike a balance in my class breaks between similar intervals,
similar counts of values, and a nice spatial pattern.

## Lab 3: Thematic Maps
![Layout_lab3-1](https://github.com/ibell13/393_carto/assets/122644517/ad4edb4c-035b-4615-bc87-b9c2233724c2)
[PDF Version](/pdfs/Layout_lab3.pdf)

In my third project, I mapped four county-level US Census datasets in Oregon using distinct map designs.
These included a dot density map of housing units in residential areas; 
a proportional symbol map of foreign-born population; a pie chart/proportional symbol map of people with college degrees; 
and a choropleth map of poverty rates.

Some compromises were made when creating these maps. On the proportional symbol map, the extreme discrepancy in foreign-born population sizes between Oregon's urban and rural counties 
forced me to set minimum and maximum point sizes. This doesn't make clear the true spread of this dataset, and makes comparing the proportionality of the dots less clear. In addition, the dot density map isn't a true density map, instead showing county-level housing density 'masked' into all of that county's residential areas.

## Lab 4: Terrain Designs
![Layout_1_lab4-1](https://github.com/ibell13/393_carto/assets/122644517/f6834a89-2f1b-4de3-b09f-76ee2f75cec1)
![Layout_2_lab4-1](https://github.com/ibell13/393_carto/assets/122644517/4b1e2afa-d446-4069-bfd2-2056d2e7b977)

- [Layout 1 PDF](/pdfs/Layout_1_lab4.pdf)
- [Layout 2 PDF](/pdfs/Layout_2_lab4.pdf)

In my fourth project, I made 8 maps of terrain features in Bryce Canyon National Park. A number of layers were created using a DTM (digital terrain model), including hillshades, contour lines, 
curvature models (varying symbology based on the shape of a surface), and hypsometric tint (varying symbology based on elevation). Other layers, like the land cover and orthoimagery (aerial/satellite 
imagery) come directly from Esri Living Atlas in ArcGIS. I combined and modified the symbology of a variety of these layers to create 8 different maps showing terrain features.
Most of these maps are at the same scale (1:37,000) and show the same area.

I also created a reference map, the eighth map shown on the layout. This uses hillshade and hypsometric tint for its basemap, with the addition of trails (dashed lines), roads, and streams from Utah's
Geospatial Resource Center website.
