# essay

<img src="img/front.png" width='950'> <br>
<img src="img/logo.png" width='300'> <br>
## The Digital Geography for the Natural Heritage Conservation Mobilization in the U.S.<br>

### :newspaper: Introduction
### A. Digital Geography<br>
Digital technology has long contributed in explaining phenomena that relates with almost all aspects of our contemporary world. The relationship between digital technology and geography took 3 forms:
- **produced through**, meaning that digital technology is aimed at actualizing unorthodox understanding to produce geographic, politics, and spatial knowledges. The engagement between the digital technology and geography has evidenced to be able to mobilize people power for social change;
- **produced by**, meaning that digital system served cities planning, management, governance, and research by integrating  urban big data, computational modelling, urban simulation, and interactions with diffent users and urban spaces;
- **geographies of digital**, meaning that the digital geographies are sets of technologies that go beyond an engagement with an interface, but with spatial big data. One of the examples is the  geotagged data retrieved from Twitter that can be used to explain sociospatial dynamics in particular area to public (James, Kitchin and Leszczynski 2018, 26-34).<br>

> With this understanding, the web map entitled **`America's Public Land Giveaway`** written by *Andre Miller* is selected for this essay. The web map provides a good example of how the integration between a story map and digital geography could increase its potentials in mobilizing civis power through rich and  evidence-based narrative. <br>

### B. Case Study<br>
The **`goal`** of the web map is *to discuss the implications of the U.S. government's policy of leasing millions of acres of public lands for private oil and gas development with unreformed rent price on natural heritage conservation efforts in the Western part of the U.S*. These natural heritage include **Dinosaur National Monument** and **critical habitats of plant and animal species** situated in 10 states: Arizona, California, Colorado, Idaho, Montana, New Mexico, Nevada, Oregon, Utah, and Wyoming. The issues revolve around:
- un-updated leasing system for oil and gas industries' operations in the West which allowed  private industrial companies to take this advantage.
- inproportionate composition between oil and gas industries uses and public uses where 90% of the land is dedicated for these industries and only 10% is left for recreational and conservation purposes.
- the Trump administration's initiative of offering 24.5 million of acres of land nationwide for these industries, hence, only about 13.5 millions of acres will be aimed for public use and conservation.
- the land price must be paid by the private companies is **below the market price**

Despite the leasing system has not yet been renewed by Congress, it has already locked up millions of acres of public land in these states for these industries. Based on the web developers' studies, many oil and gas industries produced only limited amount of these energy resources.<br>

<img src="img/dinos_abuse.png" width='900'> <br>

The developers of the web map consists of a non-profit organization for wildlife conservation, [The Wilderness Society](https://www.wilderness.org/about-us)**`﻿The Wilderness Society`** <https://www.wilderness.org/about-us> and a nonpartisan conservation and advocacy organization for the American West, **`Center for Western Priorities`** <https://westernpriorities.org/about/>.<br>

The **`major functions`** of the web map is to **convince public about negative implications of un-reformed oil and gas leasing system in the U.S. on the sustainability of natural heritage in those 10 states.** The web developers argue that ineffective leased lands could actually be utilized for social and conservation-related uses. <br>

The web map is not targeted only to particular groups, but to public audience. It serves to allow all types of users to recognize how invisible **`panopticon`** <https://www.theguardian.com/technology/2015/jul/23/panopticon-digital-surveillance-jeremy-bentham> along with its machine exercised power in the U.S.(Foucault 2014, 660). It is expected that this research-based narrative could develop public awareness on the issue and mobilize them to encourage Congress and the U.S. government to reform the land leasing system policy in the West.<br>

### :bar_chart: Systematic Architecture
To create, serve, and use web mapping,  different types machines are required. These machines are typically depicted in a diagram that consists of separate levels, or tiers of architecture. The figure below shows the **`Web Client Application`** which extends into **`External Internet`** and then, systematically continues to **`Internal Network`**, **`Web-server`** and **`Geospatial server`**. The line then branches to 2 systems: **`File Server`** and **`Database server`**. In the left part of the diagram is another computer drawing called as **`Administrators`** and **`Internal Client Application`**.<br>

<img src="img/system_arc.png" width='900'> <br>

The systematic architecture of the web map is explained as follows:
- *desktop workstations* are used by the web's administrators and internal client applications to prepare data, author maps, including administer the other machines.
- *database server* and *file server* serve as what hold the GIS data and research data of the two organizations. The data might consist of spatial data in raster or vector formats.
- *geospatial server* used to host the web services in this project is ArcGIS <https://www.esri.com/en-us/arcgis/products/geoportal-server/overview> supported by ESRI. **Esri Geoportal Server** is an open source product that since 1969 has contributed in enabling a lot of organizations to manage and publish their geospatial data and resources for wide range of users.<br>

### :lock_with_ink_pen: Code Analysis
In this part, I will discuss some important elements and codes of the web, the data that flow between client and server, web's major libraries and codes that specifically evidence its responsiveness.
<br>
*First*, the code the developers used to enable client to track any applications that supports JavaScript: <br>

```
var _paq = _paq || [];
  /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
  _paq.push(['trackPageView']);
  _paq.push(['enableLinkTracking']);
  _paq.push(['trackAllContentImpressions']);
  (function() {
    var u="https://storymaps-analytics.arcgis.com/";
    _paq.push(['setTrackerUrl', u+'analytics.php']);
    _paq.push(['setSiteId', '7']);
    var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
    g.type='text/javascript'; g.async=true; g.defer=true; g.src=u+'analytics.js'; s.parentNode.insertBefore(g,s);
  })();
```
<br>

*Second*, the code the developers used for scaling the SVG (Scalable Vector Graphics) that allow developers to set the coordinates, width and height
<br>
```
<svg viewBox="0 0 32 32" class="jsx-2552718285">
<path d="M16.707 16l10.607 10.606-.708.707L16 16.707 5.394 27.313l-.708-.707L15.293 16 4.686 5.394l.708-.707L16 15.293 26.606 4.687l.708.707z" class="jsx-2552718285">
</path>
</svg>
```
<br>

*Third*, the code the developers used for matching the web map to other widget or small gadgets:
<br>
```
div class="esri-widget--button esri-widget esri-interactive"
```
<br>

*Fourth*, the code the developers used for establishing a new coordinate system inside the element where the transformations apply to, so the units specified for the element and its children will be scaled according to the transformation :
<br>
```
g transform='matrix()'
```
<br>

### A. Data Flows Between Client and Server<br>
The data used by the wed developer come from the two nonprofit organizations' own studies and other resources which are linked to the web. These data include:<br>
- the *Federal Onshore Oil and Gas Leasing Reform Act of 1987 100th Congress (1987-1988)* <https://www.congress.gov/bill/100th-congress/house-bill/2851> to support the author's argument that the leasing system on land for oil and gas drilling was very outdated.<br>

- the *spatial distribution of federal oil and gas leases* comprising of those leased for minimum bid ($2 per acre), those leased noncompetitively (below $2 per acre), and leased under Trump administration.

<img src="img/data3a.png" width='900'><br>

- the *spatial distribution of natural heritae sites*: national parks, monuments, conservation areas, wilderness areas, prioritized sage-grouse habitat, and mule deer migration corridor<br>

<img src="img/data4.png" width='900'><br>

- the *spatial conflict* between the industries' exploration sites and the mule deer migration corridor<br>

<img src="img/data5.png" width='900'><br>

### B. Libraries<br>
Libraries used in this web map includes **css**, **js**, **jquery**, and **analytics.js**. Libraries in web-based javascript is used to provide various functions, whether the matter is related to events or effects or AJAX, and allows map developers to perform a task. The major libraries used by this web map developer along with their functions is **`analytics.js`** library with script tag:
<br>
```
script type="text/javascript" async="" defer="" src="https://storymaps-analytics.arcgis.com/analytics.js"
```

| Library                                                  | Descriptions           |
| -------------------------------------------------------- | ---------------------- |
| ![CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) | Cascading Style Sheets |
| ![JS](https://www.javascript.com/)                       | JavaScript             |
| ![JQuery](https://jquery.com/)                           | JQuery                 |
| ![Analytic](https://developers.google.com/analytics/devguides/collection/analyticsjs)|Analytic.js|

<br>
The analytics.js library has the same function as Google Analytics and is classified as a JavaScript library. The analytic.js tag's specific function is to measure how often users interact with the web map.
<br>

### C. Responsive Design<br>
A good interactive web map should be responsive to different users and settings. **Responsive design** is defined as a set of strategies for using the Open Web Platform that dynamically change the content, layout, and styling of a webpage based on the display device and user context. The examined project is a responsive web map design  because it uses **meta tags** and **div tags** elements.<br>

This meta tag tells the browser what width it should render the viewport at (*adaptive cartography*)
<br>

```
meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1"
```
<br>

With meta tag, the web map designs will change/adapt based on different use and user contexts, and the computing system could be held in hand, such as a smartphone or tablet (*mobile device*) with code:
<br>

```
meta name="mobile-web-app-capable" content="yes"
```
<br>

The div tag interlocks set of horizontal rows and vertical columns in a webpage responsively with size based on relative percentage (*fluid grid*) with code:
<br>

```
div class="page-container"
```
<br>

The div tag adds a full width containers (which spans 100% of window) inside a container which has a fixed width and aligned center. The code used by the web map is:
<br>

```
div class="container full-screen main"
```
<br>

### :books: Data Sources
### A. Data Types<br>
There are two major types of data used by the web developer: vector and raster. In terms of **vector**, the polygons in the maps indicate the different size of land parcel with different land leases. <br>

| Data type  |Format      | Descriptions |
| ------------------- | ----------------------- | ----------- |
| *geojson*  | vector | polygons that represent land lots/parcels|
| *tilelayer* | raster | land contours of the 10 states in the U.S.|

One of the codes associated with the GeoJson files can be seen from the following screenshot.<br><img src="img/geojson.png" width='800'><br>

The **raster** data is displayed through tilelayer that shows the different elevation of land in the 10 states in the U.S. The screenshot below shows the code associated with the raster.<br><img src="img/raster.png" width='800'><br>

### B. Critiques on the UI/UX<br>
The **`User Interface`** and **`User Experience`** Designs are two crucial components of a web map which work closely together. Despite their similar roles, each component has different design and process. The User Experience (UX) relates with elements that are used to effectively influence users' experience, perceptions, and easiness in accessing the web map. The UI design  focuses on the appearance, presentation, and interactivity of the web map with user. This web map's developers have integrated **`storymap with digital geography`** by thoughfully considering the kinds of experience that can be obtained by users from their web map. These experiences include:<br>

- users can expand the thematic map by clicking the icon at the top-right and  the legend at the left-bottom of the page. This makes users easily interact with the map. Clicking the expland icon again will bring the users to the original scale of map.<br><img src="img/zoom.png" width='600'><br>
- users capture the developers' emphasis after experiencing the **animated zoom** of the map provided in the page of National Dinosaur Monument.<br><img src="img/inter.png" width='600'><br>
- users can zoom in and zoom out the map with accordance to their needs<br><img src="img/inter2.png" width='600'><br>
- users can choose each item of the page/data list to revisit each page of the web<br><img src="img/inter3.png" width='600'><br>
- users can obtain details of data of each state by clicking specific area of the map.<br><img src="img/data6_interact.png" width='600'><br>
- users can highlight an area on map and obtain detailed data features. Users can also zoom in or go to next data using elements in that data box.<br><img src="img/data7_interact2.png" width='600'><br>

### :page_with_curl: Descriptions of Web Map Elements<br>
The basemap used in the webmap is attributed to those in **`Esri Gallery`** with the following script tag:
<br>
```
<script type="text/javascript" charset="utf-8" src="https://js.arcgis.com/4.15/esri/layers/TileLayer.js">
```
<br>

<img src="img/basemap.png" width='900'><br>

### C. Maps and Tile Layers<br>
There are five thematic maps used in this web map :
1. types of federal and oil gas leases map (minimum bids, noncompetitively bids, under Trump administration)
2. dinosaur national monument map
3. priority sage-grouse habitat map
4. red-desert to hoback migration map in Southern Wyoming/mule deer migration corridor
5. federal oil and gas leases still available to buy noncompetitively.<br>

The web developer used basemap tile and layers from ESRI. The scrip tag refering to **`esri`** in this web map is:
<br>
```
<script type="text/javascript" charset="utf-8" src="https://js.arcgis.com/4.15/esri/layers/TileLayer.js"
```
<br>

The interactive elements used by the web map developers include:
1. Interactive Map View
- the controlable zoom-in and zoom-out
- the GeoJson event where a layer will appear on certain pages, overlaying the visited page/map. For instance, when we scroll down the Dinosaur National Monument page, the federal oil and gas leased lands will appear and overlay the existing map of the Dinosaur National Monument map.
- the map will be enlarged as user click the expand icon on the top-right of the page/map<br>
2. Interactive Legend
- the legend will appear as user click the legend icon on the bottom-left of the page/map. <br>
Besides these two interactive elements, the other element is **interactive home icon**. It enables users to return to the first page of the web. The web developer does not use scale and compas which indicate the weaknesses of this web map.<br>

### :bulb: Strengths & Weaknesses
#### Strengths
The strengths of the web map that I identified include:
- it provides an example a responsive designed web map as it is adaptive to different users, interactive as it allows users to expand the map and legend, and mobile device friendly.
- it has interactive elements that are relatively easy to navigate and help users to explore the map, and more importantly, to obtain some details about the data used for the spatial maps. Users can also explore the page without being overwhelmed with too many options.
- it gives a suprise effect as users navigate the *Dinosaur National Monument* page where the map is automatically zooms-in. The developers bring users to the focus on the issue by zooming in the federal oil and gas leased lands that are conflicted with the heritage site.<br>

#### Weaknesses
The weaknesses of the web map are:<br>
- since each layer contains numerous amount of data featurs of 10 states, some maps in page of **mule migration corridor** for instance, has a very slow processing to be completely uploaded. This consequently requires users to have a strong network connection and high-hardware specifications with better graphic card (Roth et al. 2018).
- some data are better displayed with **`real time visualization`** so it can convey the change of the spatial structure of the leased land from 1897 to the current time. The real-time data visualization has widely been used to perform real-time monitoring of critical city infrastructure and to increase transparency (Goodchild (2010) and Hudson-Smith,Batty (2014) mentioned in Li, et al., 2019, pp. 3-10).

<img src="img/proc.png" width='900'><br>

### :thought_balloon: Discussion<br>
The web map represents an effective use of digital geography in producing a spatial knowledge in an emotional and reflexive ways (James, et al., 2018, p. 28). **Emotional** means it develops concerns and sympathy of the users participate in solving the issue. **Reflexive** means that it encourages users to reflect the conflict and mobilize to change the undesired condition.<br> Despite the effectiveness of social media in mobilizing people is highly dependent upon a lot of factors (e.g., political system of the country, government's control, literacies, internet access) (Kay, et al., 2020, p. 355), the **data crawling technique** from social media such as Twitter might be useful to inform users about public perceptions on this spatial conflict. <br>

Using a form of a story map, the web map effectively communicates its goal. The 3 narrative elements of this web map include:
<br>
1. **Set-up Act**<br>
The **settings** are the leased lands for oil and gas drilling in ten states in the U.S.: Arizona, California, Colorado, Idaho, Montana, New Mexico, Nevada, Oregon, Utah, and Wyoming. The **key characters** are the Trump administrators, Congress who still unreformed the leasing system policy, and the conservationists who defend the public rights over the needs of recreations and conservations. The **problem** is  the conflict between the U.S. government and conservationists, between the land commercialization/industrialization and natural heritage conservation. The **time** is framed within the Trump's administrative.<br>
2. **Conflict Act**<br>
The **key issue** of the story is the conflict between the U.S. government and conservationists who are compelled to protect the natural heritage conservation in the ten states in the face of unrealistic land leasing system of the U.S. Unlike a common narrative or drama, this researh-based story map is built gradually from introducing the conflict to the recommendation for future spatial planniang and policy making.<br>
3. **Resolution Act**<br>
The **recommendations/solutions** are assessing the land's suitability for oil and gas leasing through comprehensive planning processes, engaging community in the planning, raising the national minimum bid from $2.00 per acre to at least $10.00 per acre, and setting up a reliable evaluation to evaluate the lessees' capacity of exploring and producing oil and gas <br>

### :flags: Credits/Acknowledgement
The credits for this project go to:
- Andre Miller, the Wilderness Society and The Center for Western Priorities organizations for providing the inspirational story of politics-environmentalist conflict in the U.S. <br>
- Professor Bo Zhao, the instructor of the GEOG 458 for providing the lectures and materials to analyze the web map.<br>

### :link: References
[1] Andre Miller:  <https://storymaps.arcgis.com/stories/36d517f10bb0424493e88e3d22199bb3><br>
[2] James, A., Kitchin , R. & Leszczynski , A., 2018. Digital turn, digital geographies?. Progress in Human Geography, 42(1), p. 25–43.<br>
[3] Kay, S., Zhao, B. & Sui, D., 2020. Can Social Media Clear the Air? A Case Study of the Air Pollution Problem in Chinese Cities. The Professional Geographer, 67(3), pp. 351-363.<br>
[4] Kitchina, R., Maalsen, S. & McArdle, G., 2016. The praxis and politics of building urban dashboard. Geouforum, Volume 77, pp. 93-101.<br>
[5] Li, W., Batty, M. & Goodchild, M. F., 2019. Real-time GIS for smart cities. International Journal of Geographical Information Science, pp. 1-14.<br>
[6] Song, Z., 2017. Map-Based Visual StoryTelling: As Assessment of Emerging Genres and Tropes. Madison: University of Wisconsin.<br>
[7] Zhao, B., 2020. Geospatial Data for Digital Geographies; System Architecture for Web Mapping; Web Programming Basics I: HTML and CSS, Seattle: University of Washington.<br>
[8] Markdown-Guide https://about.gitlab.com/handbook/markdown-guide/#puzzle<br>

Link to the web map: <https://storymaps.arcgis.com/stories/36d517f10bb0424493e88e3d22199bb3>
