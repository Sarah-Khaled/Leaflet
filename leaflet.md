---
title: "Leaflet project"
author: "Sarah khaled"
date: "July 10, 2019"
output:
  html_document:
    keep_md: true
---
# Create a web page using R Markdown that features a university of calgary map created with Leaflet.



```r
library(leaflet)
```

```
## Warning: package 'leaflet' was built under R version 3.6.1
```

```r
# University_of_Calgary URL
University_of_Calgary <- c("<a href= 'https://www.ucalgary.ca/' >University of
                           Calgary</a>")
#creat the map
my_map<-leaflet() %>% addTiles()
# add marker on the map that refers to University of Calgary
my_map<-addMarkers(my_map,lat = 51.073166374 ,lng = -114.126499494 , popup = University_of_Calgary)
my_map
```

<!--html_preserve--><div id="htmlwidget-80c05df80e214ac55c79" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-80c05df80e214ac55c79">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[51.073166374,-114.126499494,null,null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},"<a href= 'https://www.ucalgary.ca/' >University of\n                           Calgary<\/a>",null,null,null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[51.073166374,51.073166374],"lng":[-114.126499494,-114.126499494]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
