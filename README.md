# SDS210 Wildfire Mapping

This project builds a reproducible Python workflow for mapping recent wildfire detections in Europe using the NASA FIRMS API.

## Research question

Where are the most recent and most intense wildfire detections in Europe, and how can NASA FIRMS API data be used to visualize their intensity and detection confidence on an interactive map?

## Data source

The project uses active fire detection data from the NASA FIRMS API.

The data are point based fire detections derived from satellite observations. Although the original detections come from remote sensing data, this project processes them as vector point data rather than raster data.