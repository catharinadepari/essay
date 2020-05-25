# essay

<img src="img/front.png" width='950'> <br>
### Digital Geography for Social Mobilization towards Natural Heritage Conservation in the U.S.<br>

### :newspaper: Introduction
<b>Digital Geography</b><br>
Digital technology has enabled scholars to explain the phenomena related to almost all aspects of urban living: politics, social, culture, economy, and nature. The relationship between the digital technology and geography takes at least into 3 forms: 1) **produced through**, meaning that the digital technology is aimed at actualizing unorthodox understanding to produce geographic, politics, and spatial knowledges. Despite criticsm against its use, the engagement between the digital technology and geography has proven to be able to mobilize people power for social change; 2) **produced by**, meaning that digital system served cities planning, management, governance, and research by integrating the urban big data, computational modelling, urban simulation, and interactions with diffent users and urban spaces; 3) **geographies of digital**, meaning that the digital geographies are sets of technologies that go beyond an engagement with an interface, but with spatial big data. One of the examples is the  geotagged data retrieved from Twitter that can be used to explain sociospatial dynamics in particular area to public (James, Kitchin and Leszczynski 2018, 26-34). With this understanding, the storymap entitled 'America's Public Land Giveaway' written by *Andre Miller* is selected. The storymap provides a good example of how the author carefully designed and selected the web features in order to provide deeper understanding on the implications of government's un-updated land regulation to the natural heritage and wildlife habitats in the Western side of the U.S., and to mobilize wider supports from the U.S. wide community for land conservation.
<b>The Case Study</b><br>
The goal of the storymap is *to discuss the implications of the federal government and Trump administration's policy of leasing millions of acres of public lands for private oil and gas development with low and outdated rent price on conservation sites of natural heritage in the Western part of the U.S*. These natural heritage include Dinosaur National Monument and critical habitats of plant and animal species situated in 10 states: Arizona, California, Colorado, Idaho, Montana, New Mexico, Nevada, Oregon, Utah, and Wyoming. The issue revolves around the un-updated leasing system for oil and gas industries' operations in the West. The leasing system had not been renewed since a century ago. However, the leasing has already locked up millions of acres of public land in the West. The disadvantages resulted from this are the ineffective use of the land since limited amount of oil and gas produced from the current oil and gas industries, the decrease in annual tax return at only $ 1.50 per acre for taxpayers, and risks on the natural heritage conservation. <br>
The major functions of the storymap is to mobilize public supports for encouraging the congress to modernize the oil and gas leasing system. Through this, the land could be utilized for social, cultural, and environmental purposes which include public recreation and natural heritage conservation. <br>
The audience targeted by the story map is public, particularly those who have dedications and interests in environment conservations. <br> The authors of the storymap are a non-profit organization for wildlife conservation, **`﻿The Wilderness Society`** and a nonpartisan conservation and advocacy organization for the American West, **`Center for Western Priorities`**.<br>
<img src="img/logo.png" align='center' width='200'> <br>

### :bar_chart: Systematic Architecture
Client, Server, Services, Data **`var mymap = L.map()`** for <br>

### :lock_with_ink_pen: Code Analysis
Inspect the code of this project, especially look into the following issues.
  - What are the data flowed in between the client and server.
  - The major libaries in use and their functions.
  - Does this project support responsive design?<br>

### :books: Data Sources
- vectors (i.e., geojson)
- rasters (i.e., tilelayer)
- critique its overalll UI/UX and Web Mapping design if it has.
Below is the table that shows the data library of two geometric/spatial files used in this leaflet: **`airports.geojson`** and **`us-states.geojson`**.

| **data file**      | **attribute** | **type of data** | **source** |
| ------------------ | ------------- | --------- | --------------- |
| airports.geojson   | AIRPRTX010    | Numeric    | airport tax |
| | ICAO | String | four-letter alphanumeric code designating each airport around the world, determined by International Civil Avian Organization.|
| | IATA | String | International Air Transport Association, the official trade organization for the world's airlines|
| | AIRPT_NAME | String | name of the airport in the U.S.|
| | CITY | String | the city within which the airport is located|
| | STATE | String | the state within which the airport is located |
| | COUNTY | String | the county within which the airport is located|
| | TOT_ENP | Numeric | the total number of passengers enplanned by one aircraft |
| | ELEV | Numeric | the elevation level of the airport above the sea level |
| | CNTL_TWR | Binary | the avaiilability of ATCTs where *Y* indicates availability and *N* indicates the otherwise |
| us-states.geojson | id | Numeric| identification number of the airport according to FAA. |                         |
| | name | String | name of the State where the airport is located |
| | count | Numeric | number of airports had by the state |

There are 52 features contained in the **`us-state.geojson`** file and 940 features contained in the **`airports.geojson`** file<br>

### :page_with_curl: Descriptions of Web Map Elements
Describe the basemap, the thematic layer and the interactive features if it has.
- list any web map element in use (e.g, scalar bar, north arrow, legend, etc.) if it has. <br>
-
### :bulb: Strengths & Weaknesses
- analyze the strengths and weakness of the examined project.<br>
### :thought_balloon: Discussion
- disucss anything else you feel worthy to share.
- reflect upon this project with some social theories, such as digital divide, power relationship, surveillance and/or resistance.<br>

### :flags: Credits/Acknowledgement
The credits for this project go to:
- United States Government for providing the data file through its open-sourced database.
- Mike Bostock whose website is inspirational for  further leaflet exercises and provides data file for this project.
- Carto DB for providing the basemap.
- Patiphan Phengpao whose stategy of developing live server for leaflet preview (besides Atom and Google Chrome) is highly contributive <https://www.youtube.com/watch?v=FHOcQdu1iFM>. <br>

### :link: References <br>
[1] Aviation consultant DWU:  <https://dwuconsulting.com/> <br>
