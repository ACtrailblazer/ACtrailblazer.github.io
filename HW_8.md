---
name: HW 8
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a homework project that I worked on!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Example including vega-lite

### Plot 1: Total floors and Floors Above Grade

<vegachart schema-url="{{ site.baseurl }}/assets/json/Total_Floors_Above_Grade.json" style="width: 100%"></vegachart>

### Write-up 

In this visualization, I am taking the building inventory dataset and trying to show how the amount of floors above grade changes as the number of total floors changes. There seems to be a pretty linear line/relationship between the two as expected. For this visualization, I used X and Y encoding to set the X and Y axis of the plot and used color encoding/a color scheme redyellowgreen. I selected this color scheme in order to help visualize the number of floors above grade rising. Typically you think of red as bad/low and green as good/high and that was the reasoning behind my color choice here. Behind the scenes I did some data cleaning by getting rid of the zeros in the: Square Footage, Year Acquired, and Year Constructed columns as well as disabled the max rows limitation so that I was able to capture all of the data in my visualization.

### Plot 2: Square Footage of Buildings by Year Acquired

<vegachart schema-url="{{ site.baseurl }}/assets/json/Year_Acquired_Square_Footage.json" style="width: 100%"></vegachart>

### Write-Up 

In this visualization I am comparing the Square footage of buildings across the years between different agencies. Like my previous plot, I am using X and Y encoding to set the X and Y axis of the plot and used color encoding/a color scheme rainbow. I am using the rainbow color scheme to illustrate the difference between the different agencies and I thought that the rainbow color scheme would be the best at differentiating between different ones. I didn't do HW 7 so I had no similar plots that I used. Behind the scenes I did some data cleaning by getting rid of the zeros in the: Square Footage, Year Acquired, and Year Constructed columns as well as disabled the max rows limitation so that I was able to capture all of the data in my visualization.


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

