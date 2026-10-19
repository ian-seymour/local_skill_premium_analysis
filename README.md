# Local Skill Premium Analysis
Machine learning and statistical analysis of OEWS wage data, BEA RPPs, and O*NET measures. Repo contains Jupyter Notebooks and data needed to execute the notebooks.

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

All of the data except OEWS May 2025 "All data" file has been included in the data folder, to run you will need to
download the missing file (it is too large for GitHub's limits). The file can be found at:

https://www.bls.gov/oes/special-requests/oesm25all.zip

The remaining files can be found at these links if needed or if you wish to try with newer data as it comes out.

https://www.onetcenter.org/dl_files/database/db_30_2_text.zip
https://www.bls.gov/oes/area_definitions_m2025.xlsx
https://apps.bea.gov/regional/downloadzip.htm
https://www.bea.gov/data/prices-inflation/regional-price-parities-state-and-metro-area
https://data.census.gov/table/ACSDT5Y2023.B25064?g=010XX00US$0500000

For Census, use the tool to select and download the specified tables (with filters).

## Running

1. Install the packages in 'requirements.txt' ('pip install -r requirements.txt').
2. Put the data in 'data/' (file path may differ based on OS).
3. Run all cells.

Tables are displayed in the notebook. Figures are saved to 'outputs/figures/' as PDFs.

The full run may take a few hours depending on the machine. If you want to check that everything works first, 
set QUICK_RUN = True in the next cell (it uses fewer repetitions and bootstrap) draws and skips the robustness tests,
so its numbers will not match the paper. Random seeds are fixed, so a full rerun gives the same numbers.
