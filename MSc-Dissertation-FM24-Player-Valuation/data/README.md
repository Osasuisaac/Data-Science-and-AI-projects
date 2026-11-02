# Data

The data files are not included because Football Manager 2024 data belongs to Sports Interactive / SEGA.

## Rebuilding the input file

The notebooks expect `fm_with_uefa.xlsx` in this folder. To recreate it:

1. Export player data from Football Manager 2024 for European leagues (players aged 18 and over), including name, age, position, club, division, nation, CA, PA, wage, transfer value, contract expiry and height.
2. Add two columns from the UEFA country coefficient rankings for 2023/24:
   - `country`: the country of the player's league
   - `uefa_points`: that country's UEFA coefficient
3. Save the file as `fm_with_uefa.xlsx` in this folder.

Running `notebooks/01_data_cleaning_and_preparation.ipynb` then creates:

- `fm_cleaned_ready.csv` / `.xlsx`
- `fm_with_league_strength.csv` / `.xlsx` (used by the model notebooks)
