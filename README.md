# Single-Cell Data Analysis Portfolio Project

This repository contains three end-to-end data analysis practicals focused on single-cell biology:

- Plate reader growth dynamics
- Flow cytometry induction analysis
- Live-cell imaging time-series analysis

The project is designed as both:

1. A biological data analysis study
2. A portfolio-ready demonstration of data analyst skills (data cleaning, transformation, exploratory analysis, visualization, interpretation, and reporting)

## Why This Project Matters for a Data Analyst Role

Although this dataset comes from biology, the workflow mirrors real analyst work in many industries:

- Converting messy raw files into analysis-ready tables
- Defining consistent metrics and KPIs (growth rate, lag phase, induction shift, fluorescence change)
- Comparing cohorts/segments (strains, transitions, conditions)
- Building visual narratives for decision-making
- Translating quantitative outputs into clear conclusions

## Repository Structure

- `1_practical_Platereader_Growth2025/`
  - Growth curve preprocessing, transformation, smoothing, feature extraction (`mu`, `tlag`)
  - Condition and strain-level comparisons
- `2_practical_Flow cytometry2025/`
  - Single-cell fluorescence distributions and induction kinetics across transitions
  - Control-vs-treatment interpretation and multi-view visual diagnostics
- `3_practical_Live_Cell_Imaging2025/`
  - Time-lapse single-cell trajectory analysis
  - Population- and cell-level fluorescence/morphology trends

## Core Analyst Skills Demonstrated

- Data Wrangling
  - Parsing structured filenames into metadata
  - Reshaping and joining tables
  - Handling missing/invalid values and filtering noisy observations

- Feature Engineering
  - Normalized fluorescence metrics
  - Log-transformed signals
  - Derived kinetics metrics (max growth rate, lag phase, delta fluorescence)

- Exploratory Data Analysis
  - Distribution-focused analysis (histograms, density, violin/box/strip plots)
  - Temporal trend analysis (line plots, trajectory overlays)
  - Segment-level comparison across multiple conditions

- Statistical/Modeling Components
  - Linear fitting on transformed growth curves
  - Smoothing (Savitzky-Golay)
  - Sigmoidal kinetics fitting for induction behavior

- Visualization and Reporting
  - Multi-panel figures and comparative plots
  - Heatmap summarization
  - Hypothesis-driven interpretation and biological conclusions

## Tech Stack

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook

## Reproducibility

### 1) Clone repository

```bash
git clone <your-repo-url>
cd project
```

### 2) Create and activate a virtual environment (recommended)

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3) Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scipy jupyter scikit-image
```

### 4) Run notebooks

Open notebooks in VS Code or Jupyter and run cells top-to-bottom:

- `1_practical_Platereader_Growth2025/01 Growth experiments.ipynb`
- `2_practical_Flow cytometry2025/01 Flow cytometry.ipynb`
- `3_practical_Live_Cell_Imaging2025/01 timelapse_microscopy.ipynb`

## Selected Insights (Examples)

- Plate reader: transitions ending in glucose showed higher growth rates and shorter lag phases than glucose-to-alternative-carbon transitions.
- Flow cytometry: strongest induction signal was observed in RAF->GAL conditions for GAL-reporter strains, while early GLU->GAL response was weaker.
- Live imaging: raffinose-preconditioned cells showed stronger fluorescence increase than glucose-preconditioned cells over matched time windows.

## Analyst-Focused Framing for Recruiters

If you are reviewing this project from a hiring perspective, key strengths are:

- Ability to take raw, high-volume data and produce interpretable outputs
- Strong comparative analysis across cohorts and time
- Clear documentation of assumptions and hypothesis testing
- Communication of technical results in concise business-friendly language

## Next Improvements (Planned)

- Add a `requirements.txt` or `pyproject.toml` for one-command environment setup
- Add summary dashboards (for example Plotly/Power BI style exports)
- Add lightweight automated checks for data integrity and schema consistency
- Add a short case-study style report with problem statement, KPI definitions, and executive summary

## License

See `LICENSE` for details.
