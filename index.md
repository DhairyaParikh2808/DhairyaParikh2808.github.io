---
layout: default
title: IS445
---


## Visualization 1: Top 10 License Type Distribution

<div style="text-align:center;">
    <iframe src="/assets/final_chart.html" 
            width="150%" 
            height="650px" 
            frameborder="0">
        Your browser does not support iframes.
    </iframe>
</div>

### Description of the Plot:
The first visualization is a bar chart that shows the distribution of the top 10 most common license types across cities. It displays the `License Type` on the x-axis and the count of each license type on the y-axis. The color encoding is used to differentiate each license type, making the chart more visually intuitive. The bar chart allows viewers to compare the most prevalent license types, giving them a sense of which types are most common across cities.

### Design Choices:
In this chart, I used the `x` encoding for the `License Type` to display the categorical variable on the horizontal axis, while the `y` encoding counts the number of occurrences of each license type. The color encoding is applied to differentiate the license types visually. I chose distinct colors for each type to ensure clarity and reduce ambiguity. A selection filter for `City` was added, enabling users to filter the data based on the city they are interested in. The chart also includes a tooltip feature, which displays the `License Type` and the count when hovering over the bars.

### Data Transformations:
Before plotting, I grouped the dataset by `License Type` and counted the occurrences. I then sorted the values to extract the top 10 most frequent license types. To make the chart more focused, I filtered the original dataset to include only these top 10 types.

### Interactivity:
The interactivity feature in this chart includes a city selection filter. The user can choose a city from the dropdown menu to update the chart dynamically and view the distribution of license types for that specific city. This adds a layer of granularity to the analysis, making it more relevant to individual users’ needs.

---

## Visualization 2: License Status Distribution 

<div style="text-align:center;">
    <iframe src="assets/pie_chart.html" 
            width="100%" 
            height="400px" 
            frameborder="0">
        Your browser does not support iframes.
    </iframe>
</div>

### Description of the Plot:
The second visualization is a pie chart that shows the distribution of license statuses in the dataset for the categories `ACTIVE`, `CANCELLED`, `EXPIRED`, `CLOSED`, and `INACTIVE`. The size of each slice represents the proportion of licenses in each status category. The pie chart allows users to see the relative proportions of these statuses at a glance.

### Design Choices:
For the pie chart, I used `theta` encoding to determine the size of each segment based on the count of licenses in each status. The `color` encoding differentiates the various statuses using distinct colors. The chart also includes tooltips that display the `License Status` and its corresponding count when the user hovers over any segment. The inner radius creates a donut-like appearance, which is visually appealing and leaves space for a cleaner chart without cluttering the edges with labels.

### Data Transformations:
I filtered the dataset to include only the statuses that were of interest (`ACTIVE`, `CANCELLED`, `EXPIRED`, `CLOSED`, and `INACTIVE`). Once filtered, I used the `value_counts()` function to count the occurrences of each status. This transformed data was then used to plot the pie chart.

### Interactivity:
The interactivity for this chart is built into the tooltips, which provide additional details about each segment when hovered over. This allows users to access information without cluttering the chart. Though this chart does not have other interactive elements, the tooltip provides a clear and direct way to explore the data.

---
[The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv)

[The Analysis]()