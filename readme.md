# Civic Data Deep Dive

-  
- Data literacy  chapter for the [Civic Data Education Series](https://civic-switchboard.gitbook.io/education-series/)  
	- The plan: Dive into the [CLP Public Wifi](https://data.wprdc.org/dataset/clp-public-wifi) dataset. Look at the data and come up with a *data centric question*, specifically answering the question "what neighborhood uses the most wireless?" To answer this question we need to connect the Wifi data with the [library locations](https://data.wprdc.org/dataset/libraries) dataset because that will give us GPS coordinates for each of the CLP locations. We can then use reverse geolocation with the [neighborhoods](https://data.wprdc.org/dataset/neighborhoods2) dataset to programmatically add a neighborhood information.  
	- One thing to note when you look at the [CLP Public Wifi](https://data.wprdc.org/dataset/clp-public-wifi) dataset is that the main library is far and above the most used in terms of wifi data.  
	- Idea: consider the units of the wifi usage. is it time or data? would be interesting to equate the unit to something meaningful. Like if it were data how many movies streamed.  
		- minutes.  
	- Use Sunny's [Human OGD Interaction Model](https://drive.google.com/drive/folders/1dTwqJ5Z9HpobQtc0abgS5ZUK0zfn9Bic) as a conceptual scaffolding for each of the steps.  
		- Task Preparing  
			- Generate data needs  
		- Data Foraging  
			- Find  
			- Scrutinize  
			- Acquire  
		- Data Sensemaking  
			- Understand  
			- Schematize  
		- Data Using  
			- Prepare  
			- Analyze  
			- Represent results  
			- Interpret and communicate  
		- Data Sharing  
	- Steps for video  
		- Browse the WPRDC for the CLP wifi data  
		- Look at the data, acknowledge the chart is not the data, click on the "Data Table" tab to show the actual data  
			- Go to the Data Dictionary and talk through what the columns represent.  
		- Look at the download options for the different formats (CSV, TSV, JSON, XML)  
			- Talk through and/or show the different formats?  
		- Make a note that the dateset does not include very much information about the libraries, but it does have the name and a "CLPID" code. Perhaps there is another dataset with more information on the WPRDC.  
		- On the WPRDC, browse to the other datasets provided by the Carnegie Library of Pittsburgh. Note there are 2 datasets, the wifi data which we have already seen and a "Library Locations" dataset.  
		- Browse to the "Library Locations" data and note the map representation. Again note that this is not the actual data, but rather a visual representation in map form. We don't want to download a map because we can't work with the map computationally. Click through to the Library Locations data and then navigate to the "Data Table" tab. This shows the "raw" tabular data.  
			- Go to the Data Dictionary and talk through what the columns represent.  
		- Q: at  
			-  
			-  
            
Make two or more recordings to chunk it out. only a 20 minutes.

Three videos
- looking at a dataset, specifically the Public Wifi Data. 
    - looking at it on the WPRDC website. Talking about rows and columns.
    - Downloading the data and opening in Excel.
    - Crafting Data driven questions
- Manipulating data with Python. 
    - What is Python?
    - Performing Calculations
    - Data Visualzation 
    - Answering Data Driven Questions
- Connect Datsets together
    - Joining datsets
    - Answering Questions with dervied data
    - Geospacial Visualizations



## Working Outline of the Notebook

1. Dive into the [CLP Public Wifi](https://data.wprdc.org/dataset/clp-public-wifi/resource/20843d56-506f-44b1-83df-5b16ee865783) dataset
	1. Look at the data online - Talk about the rows, columns, and what the data represents as a whole. What does each row represent.
	2. Download the data
	3. Perform some calculations with Python - aggregate the data so we can see totals for each library.
	4. Come up with a question that needs more data: What neighborhood uses the most Wifi?
	5. What additional data do we need to answer this question?
2. Dive deep into the [CLP Library Locations](https://data.wprdc.org/dataset/libraries/resource/14babf3f-4932-4828-8b49-3c9a03bae6d0?view_id=f34cd02e-17eb-40aa-8f86-ae51968db84a) dataset
	1. Look at the data online - Talk about rows and columns. What does each row represent.
	2. Note how the library locations data can be connected to the CLP Wifi Data via the "CLPID" column that is shared in both datasets. Note how this is an example of a "many to one" relationship. Many rows in the CLP Public Wifi data map to only one
	3. Download the data and load into Python
	4. Perform calculations - merge with the wifi data so we can get more information.
	5. Note there is still not enough information to determine neighborhood. But we have GPS coordinates which means we know the geographic location of each library. We can use this geographic information and merge it with geographic data representing each neighbrhood.
3. Deep dive into the [Neighborhoods](https://data.wprdc.org/dataset/neighborhoods2) dataset
	1. Look at the data. Show how the "data" is a geographic shape. Show how you can click on various points and it will pop up a table of data. One of the datapoints is the "hood" which says what neighbood the place where you clicked is in.
	2. Download the data and load into Python - Geopandas vs Pandas -  Note that this is geographic data, so it has a different shape than the tabular data. Different file formats (although it is available as a CSV file).
	3. Perform calculations - perform reverse Geolocation. We are going to programmatically "click" for each of the library locations and add the data to our dataset.
4. Talk about the final data table created from the three datasets.
# Civic Data Literacy Data Deep Dive


## Learning Objectives


## Concepts

- Finding civic data at a data repository
	- Find the [CLP Public Wifi](https://data.wprdc.org/dataset/clp-public-wifi/resource/20843d56-506f-44b1-83df-5b16ee865783) dataset
- Diving into and exploring the dataset
	- Shape of the data - tabular data
	- What are the columns?
	- What does each row represent?
- Crafting *data centric* questions
- Downloading the data
	- Data file formats (CSV, TSV, JSON, XML)
- Data Manipulation
	- Aggregations
	- Grouping
- Data Visualization
- 
