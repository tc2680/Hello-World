---
layout: post
title: Tommie's Blog Post #3
description: The Price of Water
tags: edav blog 
---

<meta charset="utf-8">

<body>

The Price of Water 
=========================================
### Introduction 
[link-un]: http://www.un.org/waterforlifedecade/scarcity.shtml
[link-water]: http://www.circleofblue.org/waternews/2010/world/the-price-of-water-a-comparison-of-water-rates-usage-in-30-u-s-cities/

<p>
According to a UN [study][link-un], water scarcity is both a natural and a human-made phenomenon. We may have enough freshwater on the planet for seven billion people but it is distributed unevenly and may be polluted in many regions.
</p>

<p>
While doing research for blog post #3, I came across a report from the [Circle of Blue][link-water] about the survey for price of water. This report provides a comparison of water rates in 30 U.S. cities and shows readers a sense of comparsion result in following infographic. 
</p>

	<img src="http://tc2680.github.io/Hello-World/bp3-waterpricingBarGraphs590" width ="400">

<p>There is also a survey table available in pdf format. </p>

	<img src="http://tc2680.github.io/Hello-World/bp3-water-survey" width ="400">

### Practice 
<p>
Since the data set is based on cities, I think it can be a good practice to try geo map which we have seen some great examples throughout the class. 
</p>

<img src="http://tc2680.github.io/Hello-World/bp3-geo-water-1" width ="400">
	
<div id='map_canvas'></div>

<script type='text/javascript' src='https://www.google.com/jsapi'></script>
<script type='text/javascript'>
      google.load('visualization', '1', { 'packages': ['geomap'] });
      google.setOnLoadCallback(drawMap);

      function drawMap() {
          var data = google.visualization.arrayToDataTable([
        ['City', 'Water Pricing'],
        ['Phoenix', 11.02],
        ['Fresno', 15.99],
        ['Memphis', 16.02],
        ['Chicago', 16.08],
        ['Baltimore', 19.25],
        ['New York', 20.88],
        ['San Antonio', 12.21],
        ['Salt Lake City', 14.48],
        ['Los Angeles', 27.18],
        ['Seattle', 42.15],
        ['Santa Fe', 43.28],
        ['Charlotte', 14.16],
        ['Dallas', 16.16],
        ['Las Vegas', 17.18],
        ['Tucson', 17.46],
        ['Denver', 18.24],
        ['Austin', 19.18],
        ['Jacksonville', 19.54],
        ['Houston', 21.97],
        ['Fort Worth', 22.2],
        ['Columbus', 23.95],
        ['San Jose', 24.51],
        ['Philadelphia', 27.34],
        ['San Francisco', 30.63],
        ['Boston', 31.84],
        ['Atlanta', 33.83],
        ['San Diego', 44.05],
        ['Milwaukee', 16.11],
        ['Detroit', 16.22],
        ['Indianapolis', 25.24]
      ]);

          var options = {};
          options['region'] = 'US';
          options['colors'] = [0xBDEDFF, 0x82CAFF, 0x2B65EC]; //marker colors
          options['dataMode'] = 'markers';
          colorAxis: { colors: ['#BDEDFF', '#x2B65EC'] }
          options['width'] = '800px'
          options['height'] = '500px'

          var container = document.getElementById('map_canvas');
          var geomap = new google.visualization.GeoMap(container);
          geomap.draw(data, options);
      };
  </script>
  
</body>
	

