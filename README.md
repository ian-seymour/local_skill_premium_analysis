# Local Skill Premium Analysis
Machine learning and statistical analysis of OEWS wage data, BEA RPPs, and O*NET measures. Repo contians Jupyter Notebooks and data needed to execute the notebooks.

This notebook produces the tables, figures, and numbers in the paper.

## Data

Put these files in a data folder (unzipped) in the same directory as the notebook. Subfolders are fine, and the original download
names work as they are because the notebook finds each file by its name pattern (so it may work for future releases if naming 
convention changes).

O*NET 30.2 Database (text file version)
OEWS May 2025 "All data" national, state, and area file
OEWS area definitions, May 2025 metropolitan and nonmetropolitan areas
BEA Regional Price Parities, state (SAIRPD) and metropolitan-area (MARPP) tables
ACS county rents, Table B25064 (median gross rent), 5-year estimates, all U.S. counties

## Running

1. Install the packages in 'requirements.txt' ('pip install -r requirements.txt').
2. Put the data in 'data/' (file path may differ based on OS).
3. Run all cells.

Tables are displayed in the notebook. Figures are saved to 'outputs/figures/' as PDFs.

The full run may take a few hours depending on the machine. If you want to check that everything works first, 
set QUICK_RUN = True in the next cell (it uses fewer repetitions and bootstrap) draws and skips the robustness tests,
so its numbers will not match the paper. Random seeds are fixed, so a full rerun gives the same numbers.
