---
name: Vega Lite Example Project
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
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


We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/cars.json" style="width: 100%"></vegachart>

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

```
<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html" text="The Analysis" %}
</div>
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>

