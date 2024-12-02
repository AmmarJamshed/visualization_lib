
`visualization_lib` is a Python library that helps with automatic data cleaning and visualization. It provides functions to clean missing data, encode categorical variables, and visualize the relationships between features and the target variable.

# Visualization Library Usage

This README provides instructions for using the `visualization-lib` library to create various types of visualizations (line plot, bar plot, scatter plot) from a dataset.

## Installation

Before using the visualization functions, you need to install the `visualization-lib`. You can do this via `pip`:

pip install visualization-lib


pip install pandas
pip install visualization-lib
Usage
``` Import Libraries
Import necessary libraries to work with data and create visualizations
```


import pandas as pd
import visualization_lib
from visualization_lib import visualizer
Prepare Your Data
Ensure you have a pandas DataFrame (df) containing the relevant data. Below is an example of a DataFrame structure:

python
Copy code
df = pd.DataFrame({
    'Purchase_Date': ['2023-01-01', '2023-01-02', '2023-01-03'],  # Example Date
    'Final_Price(Rs.)': [1000, 1500, 1200]  # Example Prices
})
Extract Columns for Plotting
Extract the columns that you want to plot:

python
Copy code
x = df['Purchase_Date']
y = df['Final_Price(Rs.)']
Create Visualizations
Create an instance of the Visualizer class and generate different plots:

python
Copy code
viz = visualizer.Visualizer()

# Line Plot
viz.line_plot(x, y, xlabel="Date", ylabel="Sales", title="Line Plot of Sales")

# Bar Plot
viz.bar_plot(x, y, xlabel="Date", ylabel="Sales", title="Bar Plot of Sales")

# Scatter Plot
viz.scatter_plot(x, y, xlabel="Date", ylabel="Sales", title="Scatter Plot of Sales")
``` Plot Types
Line Plot: Displays data points as a continuous line.
Bar Plot: Displays data points as bars.
Scatter Plot: Displays data points as scattered points on the graph.
```

Ensure that your data is in the correct format for the x (dates) and y (values) columns.
Customize plot titles and labels as needed.
``` Example ```

import pandas as pd
import visualization_lib
from visualization_lib import visualizer

# Sample data
df = pd.DataFrame({
    'Purchase_Date': ['2023-01-01', '2023-01-02', '2023-01-03'],
    'Final_Price(Rs.)': [1000, 1500, 1200]
})

# Extract columns for plotting
x = df['Purchase_Date']
y = df['Final_Price(Rs.)']

# Initialize the Visualizer
viz = visualizer.Visualizer()

# Create Line Plot
viz.line_plot(x, y, xlabel="Date", ylabel="Sales", title="Line Plot of Sales")

# Create Bar Plot
viz.bar_plot(x, y, xlabel="Date", ylabel="Sales", title="Bar Plot of Sales")

# Create Scatter Plot
viz.scatter_plot(x, y, xlabel="Date", ylabel="Sales", title="Scatter Plot of Sales")
