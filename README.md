# Hawker Stall Revenue Analysis

Exploratory data analysis of daily revenue across Singapore hawker stalls. The project investigates how pricing, location, cuisine type, competition, and stall age influence revenue — uncovering a Simpson's Paradox in the price–revenue relationship and resolving it through multiple regression and Monte Carlo simulation.

## Discoveries

| # | Topic | Key Question |
|---|-------|--------------|
| 1 | Revenue Landscape | What does the distribution of daily revenue look like across locations and cuisines? |
| 2 | Price vs Revenue Paradox | Why does a naive correlation suggest higher prices hurt revenue? |
| 3 | Multiple Regression | After controlling for confounders, what is the true price effect? |
| 4 | Hypothesis Testing | Is the price coefficient statistically significant? |
| 5 | Monte Carlo Simulation | What happens to expected revenue if a stall raises prices by $1–$2? |

## Dataset

`Hawker Data Statistics.csv` — 500 observations with the following variables:

| Variable | Type | Description |
|----------|------|-------------|
| `daily_revenue` | numeric | Daily revenue in SGD |
| `avg_price` | numeric | Average dish price in SGD |
| `location_type` | categorical | CBD or HDB |
| `cuisine_type` | categorical | Chinese, Malay, Indian, or Western |
| `competition` | integer | Number of nearby competing stalls |
| `day_type` | categorical | Weekday or Weekend |
| `stall_age` | numeric | Years the stall has been operating |

## Prerequisites

You need **R** and **Jupyter** with an R kernel installed.

### 1. Install R

- **macOS** (Homebrew): `brew install r`
- **Ubuntu/Debian**: `sudo apt install r-base`
- **Windows**: download the installer from [CRAN](https://cran.r-project.org/)

### 2. Install the R kernel for Jupyter

Open an R console and run:

```r
install.packages("IRkernel")
IRkernel::installspec()
```

### 3. Install R packages

The notebook depends on a single extra package. From an R console:

```r
install.packages("e1071")
```

### 4. Install Jupyter

If you don't already have Jupyter:

```bash
pip install jupyterlab
```

## Running the Notebook

```bash
# clone the repo
git clone https://github.com/<your-username>/hawker-data-analysis.git
cd hawker-data-analysis

# launch Jupyter
jupyter lab
```

Open `discovery.ipynb` and run all cells. The notebook reads `Hawker Data Statistics.csv` from the project root, so make sure you launch Jupyter from the repo directory.

## Project Structure

```
hawker-data-analysis/
├── discovery.ipynb              # Main analysis notebook (R kernel)
├── Hawker Data Statistics.csv   # Source dataset (500 rows)
├── slides/                      # Weekly lecture materials
│   ├── Week 1  – Probability measure
│   ├── Week 2  – Conditional probabilities
│   ├── Week 3  – Random variables
│   ├── Week 4  – Expectation
│   ├── Week 5  – Bivariate distributions & correlations
│   ├── Week 6  – Sampling & statistical inferences
│   ├── Week 7  – Confidence intervals
│   ├── Week 8-9 – Hypothesis testing
│   ├── Week 10 – Regression analysis 1
│   ├── Week 11 – Regression analysis 2
│   └── Week 12 – Simulation analysis
└── README.md
```
