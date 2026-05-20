# SDS210 Wildfire Mapping Project

## Project overview

This project analyzes recent wildfire detections in Europe using data from the NASA FIRMS API. The goal is to explore wildfire intensity and their spatial distribution and to visualize the detections on an interactive map.

The workflow includes downloading raw wildfire data, cleaning and analyzing the dataset, identifying the strongest wildfire detections and creating an interactive Folium map.



## Research question

Where are recent wildfires in Europe occurring, and how intense and reliable are the detected wildfire events?



## Data source

The wildfire data is downloaded from the NASA FIRMS API using the VIIRS SNPP NRT dataset.

Please get your own API key to access the API:
https://firms.modaps.eosdis.nasa.gov/api/map_key




## How to use the project


### 1. Clone the repository

Open the terminal and clone the repository:

```bash
git clone https://github.com/pascalandreasheiniger-max/sds210-wildfire-mapping.git
```



### 2. Open the project folder

Navigate into the project folder:

```bash
cd sds210-wildfire-mapping
```



### 3. Install the required packages

Install all required Python libraries:

```bash
pip install -r requirements.txt
```



### 4. Create your config file

After requesting your personal NASA FIRMS API key, open:

```text
config_template.py
```

Insert your API key:

```python
MAP_KEY = "your_api_key"
```

Then rename the file to:

```text
config.py
```




### 5. Open the notebook

Open:

```text
notebooks/wildfire_mapping.ipynb
```




### 6. Run the notebook

Run all notebook cells from top to bottom.




### 7. API mode and offline mode

Set:

```python
USE_API = True
```

to download new wildfire detections from the NASA FIRMS API.

Set:

```python
USE_API = False
```

to use the previously saved raw wildfire dataset in offline mode without sending a new API request.




## Workflow

The project follows this workflow:

1. Download recent wildfire detections from the NASA FIRMS API.

2. Inspect and clean the dataset by selecting the most relevant variables and converting the date column into a proper datetime format.

3. Analyze the wildfire detections by exploring confidence levels, fire intensity values and the strongest wildfire events.

4. Use reverse geocoding to identify the countries of the ten strongest wildfire detections.

5. Create a GeoDataFrame from the wildfire coordinates and visualize the detections on an interactive Folium map.

6. Save the cleaned dataset, analysis outputs and the final interactive wildfire map.




## Project structure

```text
sds210-wildfire-mapping/
│
├── data/
│   ├── raw/               # Raw wildfire data from the API
│   └── processed/         # Cleaned wildfire data
│
├── notebooks/
│   └── wildfire_mapping.ipynb
│
├── outputs/               # Final outputs and interactive map
│
├── requirements.txt
├── .gitignore
├── config_template.py
└── README.md
```




## Outputs

The project creates several output files:

- cleaned wildfire dataset (folder processed)
- top wildfire detections CSV (folder outputs)
- interactive wildfire map as HTML file (folder outputs)



## Author

Pascal Heiniger
