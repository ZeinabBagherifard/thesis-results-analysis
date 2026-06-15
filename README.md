# Thesis Results Analysis

Data analysis pipeline for a master's thesis user study comparing **2D Label** and **3D Ghost** situated visualization conditions in a VR-simulated AR industrial training task.

## Overview

This repository contains a Jupyter Notebook that:

- Loads raw study datasets exported as CSV files
- Merges them using `Scene` and `Participant`
- Creates a processed **wide-format** dataset
- Converts the merged table to **long format** (`variable` / `value`) for plotting
- Calculates descriptive statistics for the main study metrics
- Produces comparison **boxplot figures** and saves them as PNG files
- Summarizes the main results with numbers

## Visualizations

### Completion Time, SUS, and NASA-TLX

![Boxplots for Completion Time, SUS Score, and NASA-TLX Score](img-results1.png)

### Discomfort / SSQ Metrics

![Boxplots for SSQ discomfort metrics](img-results2.png)

## Key Findings

This analysis was conducted on data from a controlled user study with **24 participants**, comparing **2D Label** and **3D Ghost** visualization conditions.

* **Task Completion Time:** The 3D Ghost condition had a lower median completion time (**116.99s**) than the 2D Label condition (**137.66s**), showing faster task completion.
* **Usability:** The 2D Label condition had a slightly higher median SUS score (**87.5**) than the 3D Ghost condition (**85.0**). Both conditions were above the common SUS benchmark of **68**.
* **Workload:** The 3D Ghost condition showed slightly lower median NASA-TLX workload (**3.33**) than the 2D Label condition (**3.50**).
* **Overall Discomfort:** The 3D Ghost condition had a lower median SSQ score (**14.96**) compared with the 2D Label condition (**29.92**).
* **Nausea:** The 3D Ghost condition had a lower median nausea score (**0.00**) compared with the 2D Label condition (**9.54**).
* **Oculomotor Strain:** The 3D Ghost condition had a lower median score (**15.16**) than the 2D Label condition (**30.32**).
* **Disorientation:** The median disorientation score was the same in both conditions (**27.84**).

Overall, the **3D Ghost** condition showed faster task completion and lower nausea, oculomotor strain, and overall SSQ discomfort, while the **2D Label** condition showed slightly higher perceived usability.

## Tools and Technologies

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook
- Data cleaning and transformation
- Questionnaire analysis
- Boxplot visualization

## Files

- `_results.ipynb` — main notebook for loading, merging, reshaping, analyzing, and plotting the study data
- `CompletionTime.csv` — raw task completion time data
- `Nasa.csv` — raw NASA-TLX workload data
- `SSQ.csv` — raw Simulator Sickness Questionnaire data
- `SUS.csv` — raw System Usability Scale data
- `data_short_format.csv` — generated wide-format dataset, one row per participant and condition
- `data_long_format.csv` — generated long-format dataset used for plotting
- `img-results1.png` — boxplots for Completion Time, SUS Score, and NASA-TLX Score
- `img-results2.png` — boxplots for SSQ/discomfort metrics

## Expected input CSV files

These raw files should be in the same folder as `_results.ipynb` before running:

- `CompletionTime.csv`
- `Nasa.csv`
- `SSQ.csv`
- `SUS.csv`

Each dataset includes the shared identifiers:

- `Scene`
- `Participant`

## How to run

1. Make sure the required Python libraries are available:
   - `pandas`
   - `matplotlib`
   - `seaborn`
2. Open `_results.ipynb` in Jupyter Notebook.
3. Run all cells.

## Outputs

After running the notebook, you will have:

- Merged dataset: `data_short_format.csv`
- Long-format dataset: `data_long_format.csv`
- Figures: `img-results1.png`, `img-results2.png`
