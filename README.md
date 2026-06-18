# Single-Cell Data Analysis Project

This repository contains four end-to-end data analysis practicals focused on single-cell biology:

- Plate reader growth dynamics
- Flow cytometry induction analysis
- Live-cell imaging time-series analysis
- smFISH image-based quantification and visualization

The notebooks follow a full analysis workflow: loading raw data, cleaning and transforming it, extracting features, comparing conditions, and summarizing results with clear plots and interpretations.

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
- `4_practical_smFISH2025/`
  - Spot-level transcript quantification in CY3 and CY5 channels
  - Cleanup, condition parsing, and comparative visualizations for smFISH datasets

## Analysis Skills Demonstrated

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
- `4_practical_smFISH2025/napari_practical/notebooks/01 data plotting.ipynb`
- `4_practical_smFISH2025/napari_practical/notebooks/02 data cleanup.ipynb`
- `4_practical_smFISH2025/napari_practical/notebooks/03 smFISH data visualisation.ipynb`

### 5) Note on smFISH files

The smFISH plotting notebook expects intermediate pickle outputs generated from the napari practical:

- `cy3_spots.pkl`
- `cy5_spots.pkl`
- `segmentation.pkl`

Place these files in:

- `4_practical_smFISH2025/napari_practical/`

## Selected Insights (Examples)

- Plate reader: transitions ending in glucose showed higher growth rates and shorter lag phases than glucose-to-alternative-carbon transitions.
- Flow cytometry: strongest induction signal was observed in RAF->GAL conditions for GAL-reporter strains, while early GLU->GAL response was weaker.
- Live imaging: raffinose-preconditioned cells showed stronger fluorescence increase than glucose-preconditioned cells over matched time windows.
- smFISH: transcript-count distributions differ by condition and channel, and the cleanup/visualization pipeline supports direct condition-level comparisons.

## Next Improvements (Planned)

- Add a `requirements.txt` or `pyproject.toml` for one-command environment setup
- Add summary dashboards (for example Plotly/Power BI style exports)
- Add lightweight automated checks for data integrity and schema consistency
- Add a short case-study style report with problem statement, KPI definitions, and executive summary

## Data Note

Large raw microscopy TIFF files are not tracked in git to keep the repository lightweight and push-safe. The repository includes practical notebooks, processed outputs, and example data needed to reproduce the analysis workflow.

## License

See `LICENSE` for details.
