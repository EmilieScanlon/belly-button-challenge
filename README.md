# belly-button-challenge

Bacteria Cultures Dashboard

This project creates an interactive dashboard to display bacteria cultures found in different samples. The dashboard consists of two charts: a bubble chart and a bar chart, as well as a metadata panel that displays information about the selected sample.

Code Overview

The code is organized into four main functions:

buildMetadata(sample): Builds the metadata panel for the selected sample.
buildCharts(sample): Builds both the bubble chart and the bar chart for the selected sample.
init(): Initializes the dashboard by populating the dropdown menu with sample names and building the charts and metadata panel for the first sample.
optionChanged(newSample): Updates the charts and metadata panel when a new sample is selected from the dropdown menu.
Function Details

buildMetadata(sample)
Loads the samples.json file using d3.json().
Filters the metadata for the object with the desired sample number using find().
Uses d3 to select the panel with id #sample-metadata and clear any existing metadata.
Appends new <p> tags for each key-value in the filtered metadata using Object.entries() and forEach().
buildCharts(sample)
Loads the samples.json file using d3.json().
Filters the samples for the object with the desired sample number using filter().
Extracts the otu_ids, otu_labels, and sample_values from the filtered sample.
Builds a bubble chart using Plotly with the extracted data.
Builds a bar chart using Plotly with the top 10 bacteria cultures found.
Renders both charts using Plotly.newPlot().
init()
Loads the samples.json file using d3.json().
Extracts the list of sample names from the data.
Populates the dropdown menu with the sample names using d3.
Builds the charts and metadata panel for the first sample using buildCharts() and buildMetadata().
optionChanged(newSample)
Updates the charts and metadata panel when a new sample is selected from the dropdown menu.
Calls buildCharts() and buildMetadata() with the new sample ID.
Dependencies

d3.js for data manipulation and visualization.
Plotly for chart rendering.
Usage

Open the HTML file in a web browser.
Select a sample from the dropdown menu to update the charts and metadata panel.