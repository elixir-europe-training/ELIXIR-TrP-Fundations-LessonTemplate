# Creating Scientific Visualisations

Scientific visualisations are essential for making complex data and concepts more accessible and interpretable. This chapter provides a practical guide to creating high-quality visualisations using a range of tools, including traditional programming libraries, diagram creation software, and AI-powered solutions. Best practices for embedding visuals into documents and web pages will be provided.

## 5.1. Overview of Scientific Visualisations

A scientific visualisation is the process of representing scientific data graphically to enhance understanding, interpretation, and communication. It transforms complex datasets into visual formats, such as **graphs**, **charts**, **maps**, and **3D models**, making patterns, trends, and relationships more accessible.


### 5.1.1. Importance of visuals in making scientific concepts accessible.

**Enhancing Comprehension**: Visuals help convey complex scientific data in an intuitive and digestible manner, making information easier to understand.

**Facilitating Pattern Recognition**: Graphs and charts highlight trends and correlations that might not be immediately apparent in raw data.

**Improving Communication**: Well-designed visuals allow scientists to effectively share findings with both experts and non-experts.

**Supporting Decision-Making**: In fields like medicine and environmental science, data visualisations aid in making evidence-based decisions.

**Engagement and Retention**: Research shows that visual content is processed faster and remembered longer compared to text-based information.


### 5.1.2. How Scientific Visualisations Differ from General Data Visualisations

**Purpose and Context**: Scientific Visualisations are used in research and academia to represent complex datasets, simulations, or models in fields like bioinformatics, physics, and climate science. General Data Visualisations, were commonly used in business, marketing, and journalism for trend analysis, performance metrics, and storytelling.

**Complexity of Data**:

Scientific visualisations often deal with multidimensional, high-resolution, or real-time data requiring advanced computational techniques. General data visualisations typically present summarised trends in simple formats like bar charts and pie charts.

**Precision and Accuracy**:

Scientific visualisations must adhere to strict accuracy standards to ensure reproducibility and credibility. General visualisations may prioritise aesthetics and simplicity over absolute precision.


### 5.1.3. Tools for Creating Visualisations - Traditional tools

**R (ggplot2)**

***Installing ggplot2***

To install and load ggplot2 in R, use the following commands:

install.packages("ggplot2")
library(ggplot2)

***Creating a Basic Scatter Plot***

data(mtcars)
ggplot(mtcars, aes(x = wt, y = mpg)) +
  geom_point() +
  labs(title = "Scatter Plot of Car Weight vs. MPG", x = "Weight", y = "Miles Per Gallon")

***Customising Colours, Legends, and Axes***

ggplot(mtcars, aes(x = wt, y = mpg, colour = factor(cyl))) +
  geom_point(size = 3) +
  scale_colour_manual(values = c("red", "blue", "green")) +
  labs(title = "Scatter Plot of Car Weight vs. MPG", colour = "Cylinders")

**Python (Matplotlib, Seaborn, Plotly)**

***Creating a Simple Plot with Matplotlib***

import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 25, 30, 40]

plt.plot(x, y, marker='o', linestyle='-', color='b')
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.title("Basic Line Chart")
plt.show()

***Using Seaborn for Advanced Statistical Visualisations***

import seaborn as sns
import pandas as pd

# Load example dataset
data = sns.load_dataset("iris")
sns.pairplot(data, hue="species")
plt.show()

***Generating Interactive Charts with Plotly***

import plotly.express as px

data = px.data.gapminder()
fig = px.scatter(data, x="gdpPercap", y="lifeExp", color="continent", size="pop", hover_name="country", log_x=True)
fig.show()



## AI Tools for Visualisations

Introduction to AI-powered visualization tools like Napkin AI.
How Napkin AI simplifies diagram creation and ideation through natural language inputs.
Use cases: Generating concept maps, flow diagrams, and data-driven visuals quickly.

## Embedding Visuals

Best practices for saving and exporting visuals (SVG, PNG, or PDF formats).
Integrating visuals into Markdown and HTML.
