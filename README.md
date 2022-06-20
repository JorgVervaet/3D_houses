# 3D_houses

3D House final program is the complete program to input an adres and get a 3D plot of that adres.

It is programmed and tested in Python 3.10.5 and 3.9.12

You will need the following libraries:
    - earthpy
    - requests
    - plotly
    - rasterio
    - shapely


Usage is simple: You start the program then input the street you want to see, then the housenumber and then the zipcode and you get the 3D plot

Steps I took to make this program:

1. I downloaded 1 dsm and 1 dtm file and see what was in it. We got a .shp .dbf .sbn .sbx .shp.xml .shx and a .tif file

2. Researched the most important files are the tif and the shp files. Then we found out that we could use an api to get the coordinates we need and we didn't need the shp file anymore.

3. With the api we could get the polygon coordinates of a certain adres. It took some work to get the correct links everytime out of the output of the api.

4. When we got the polygon coordinates we have to compare them to the tif files we have to see which files we exactly need.

5. When we know which dsm and dtm file we need we can subtract the dtm from the dsm file to get our chm (canopy height model). This is our house that we will need to plot.

6. Then we plotted the house (the chm) in 3D

7. Finally we glued everything to gather and automated it

8. Write this README.md file

## Contributors!

I would love to thank Theano for all the support and help on this project. Especially Chrysanthi and Louis our coaches and Yihui, Rana and Pragati

Included in this directory is a jpeg (screenshot) of the result of Sint-Pietersvliet 7, 2000 Antwerpen which is our campus of BeCode

<img src="House example.jpg">
