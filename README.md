# Using within-day hive weight changes to measure environmental effects on honey bee colonies

This repository contains the Python code and instructions necessary to replicate the analysis presented in the "Using within-day hive weight changes to measure environmental effects on honey bee colonies" paper using the Osyris Replicate python package. The paper analyzes hive weight data to understand honey bee colony behavior and the impact of landscape using piecewise regression, showing how weight changes correlate with forager activity and how access to natural forage affects these dynamics.

## Steps to Replicate the Analysis

### Getting started
Install and import the package

`pip install osreplicate`\
`from osreplicate import Paper`

### Access the paper you want to replicate
Provide the papers alias to start analyzing

`analysis = Paper('plos/Environmental effects on honey bee colonies')`

### Get the datasets
Locally download any available datasets associated with this paper

`analysis.get_data()`

### Replicate the paper
Automatically run the full analysis on the available datasets and reproduce the figures from the paper

`analysis.run()`

### Mix and match      
Access core analysis methods from to the paper

`analysis.analyze_active_period_weight_changes(data, sunrise_time, sunset_time)`\
`analysis.apply_segmented_regression(data, initial_breakpoints, max_iterations=100)`\
`analysis.estimate_breakpoints_using_segmented_function(data, preferred_number_of_breakpoints)`
`analysis.model_hive_weight_during_quiescent_periods(data, start_time, end_time)`

