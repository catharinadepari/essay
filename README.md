# essay

<img src="img/leaflet_airport.png" width='950'> <br>
## Resilience Story of New York in the Face of COVID-19<br>

### :newspaper: Introduction
The aim of this project is to  **`ATCTs`** introduce this digital-geography project, including, but not limited to,
  - the goal of this project (why this project was made?)
  - the major functions
  - the targeting audience
  - the authors and their affilication<br>

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
#### :bulb: Strengths & Weaknesses
- analyze the strengths and weakness of the examined project.
#### :thought_balloon: Discussion
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
