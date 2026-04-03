# 📊 Matplotlib – Python Data Visualization Library

A beginner-friendly learning notebook covering the fundamentals of **Matplotlib**, one of the most popular Python libraries for creating charts and graphs.

---

## 📌 What is Matplotlib?

Matplotlib is a Python library used to **visualize data** — turning boring numbers and text into colorful, meaningful charts and graphs.

It is widely used in fields such as:
- **Data Science** – simplifying data exploration
- **Business / Marketing** – presenting trends and insights
- **Healthcare** – visualizing patient data
- **Finance** – tracking market performance
- **Education** – illustrating concepts visually
- **Government / Policy** – communicating research findings

> **Original Author:** John D. Hunter

---

## ⚙️ Setup & Import

```python
import matplotlib.pyplot as plt
# matplotlib → main package
# pyplot → module inside matplotlib that provides ready-made plotting functions
```

---

## ✅ Top 5 Advantages of Data Visualization

1. **Saves Time** – Quickly understand large datasets
2. **Easy Communication** – Share insights with non-technical audiences
3. **Spot Trends and Patterns** – Identify what's hidden in raw data
4. **Better Decision Making** – Act on evidence, not guesses
5. **Handles Big Data Wall** – Manage and interpret large volumes of data

---

## 📈 Chart Types Covered

### 1. Line Chart (`plt.plot`)
Used to show trends over time or ordered categories.

```python
name = ['Malaika', 'Madhuri', 'Mansi', 'Madhavi', 'Madhurima']
marks = [90, 56, 23, 60, 37]

plt.plot(name, marks, color='blue', marker='o', linestyle='dashed')
plt.xlabel("Name")
plt.ylabel("Marks")
plt.title("Marks of Students")
plt.show()
```

---

### 2. Bar Chart (`plt.bar`)
Used to **compare different categories** of data with vertical or horizontal bars with heights proportional to the values.

```python
names = ['Malaika', 'Alice', 'EMMA', 'sofi']
marks = [98, 45, 67, 23]

plt.bar(names, marks, color="#A67890", width=0.4)
plt.ylim(0, 100)     # Set Y-axis limits
plt.grid()
plt.xlabel("Names of Students", color="blue")
plt.ylabel("Marks Obtained")
plt.title("Student Result Analysis")
plt.show()           # Display the plot on screen
```

#### Bar Chart with Individual Bar Colors

```python
fig, ax = plt.subplots()

fruits  = ['apple', 'strawberry', 'banana', 'mango']
counts  = [40, 100, 75, 90]
bar_colors = ["#F01010", "#E60C79", "#F0F010", "#FDAB13"]

ax.bar(fruits, counts, color=bar_colors, label=['red','pink','yellow','orange'])
ax.set_ylabel("Fruit Counts")
ax.set_title("Fruit Count Analysis")
plt.legend(title="Fruit Colors")
plt.show()
```

#### Horizontal Bar Chart (`plt.barh`)

```python
names = ['Malaika', 'Alice', 'Emma', 'sofi']
marks = [76, 34, 89, 23]

plt.barh(names, marks, color="#3E6385")
plt.xlim(0, 100)
plt.grid()
plt.title("Student Result Analysis – Horizontal Bar Chart")
plt.show()
```

---

### 3. Pie Chart (`plt.pie`)
A **circular statistical graphic** divided into slices to illustrate numerical proportions. Each slice's arc length is proportional to the quantity it represents.

```python
plt.pie(
    x=[25, 67, 12, 45, 77],
    labels=['malaika', 'alice', 'emma', 'sofi', 'Bob'],
    colors=['red', 'blue', 'green', 'yellow', 'orange']
)
plt.title("Student Marks Distribution", size=21)
plt.show()
```

#### Key Pie Chart Features

| Feature | Parameter | Description |
|--------|-----------|-------------|
| Percentage labels | `autopct='%1.1f%%'` | Shows `%` on each slice (`f`=float, `.1`=1 decimal) |
| Hatch patterns | `hatch=['/','x','O.O','*','.||.']` | Fill slices with patterns |
| Swap label positions | `labeldistance`, `pctdistance` | Control where text appears |
| Explode slices | `explode=(0,0,0.2,0,0.1)` | Pull slices outward |
| Shadow effect | `shadow=True` | Add a shadow |
| Rotation | `startangle=90` | Rotate the chart |
| Size control | `radius=1.5` or `radius=0.5` | Make the chart bigger or smaller |

---

### 4. Histogram (`plt.hist`)
A visual way to show **how data is distributed** — groups values into bins (ranges) and draws bars representing frequency.

```python
scores = [45, 67, 89, 23, 56, 78, 90, 34, 67, 88, 92, 55, 72, 88, 91]

plt.hist(scores, bins=5)
plt.xlabel('Scores')
plt.ylabel('Frequency')
plt.title('Test Score Distribution')
plt.show()
```

#### Key Histogram Parameters

| Parameter | Description |
|-----------|-------------|
| `bins` | Number of bins/ranges (more = more detail) |
| `color` | Bar fill color |
| `edgecolor` | Border color of bars |
| `alpha` | Transparency (0–1) |

#### Normal Distribution Example

```python
import numpy as np

data = np.random.normal(loc=70, scale=10, size=1000)

plt.hist(data, bins=30, color='green', edgecolor='black')
plt.xlabel('Values')
plt.ylabel('Frequency')
plt.title('Perfect Tower')
plt.show()
```

#### Multicolor Histogram

```python
counts, bins, patches = plt.hist(data, bins=30, edgecolor='black')

for patch, color in zip(patches, np.random.rand(30, 3)):
    patch.set_facecolor(color)

plt.title('Multicolor Tower')
plt.show()
```

---

## 🛠️ Useful Utility Functions

| Function | Purpose |
|----------|---------|
| `plt.xlabel()` | Set X-axis label |
| `plt.ylabel()` | Set Y-axis label |
| `plt.title()` | Set chart title |
| `plt.show()` | Display the chart |
| `plt.grid()` | Add a background grid |
| `plt.xlim()` / `plt.ylim()` | Set axis limits |
| `plt.legend()` | Add a legend |
| `plt.subplots()` | Create multiple plot areas |

---

## 📦 Prerequisites

- Python 3.x
- Matplotlib (`pip install matplotlib`)
- NumPy (`pip install numpy`) — used for generating sample data

---

## 📁 File Structure

```
matplotlib.ipynb   ← Main learning notebook
README.md          ← This file
```

---

## 🙌 Acknowledgements

This notebook was created for **public learning purposes** to help beginners get started with data visualization in Python using Matplotlib.
