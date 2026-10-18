# Malaria Importation in Zanzibar

Exploratory data analysis of how travel between Zanzibar and mainland Tanzania may be linked to malaria cases, using Python.

This notebook is part of my talk proposal for **PyCon Tanzania 2026**.

## Background

Zanzibar has made great progress against malaria, but imported cases from the mainland make full elimination hard. This project explores a clinic dataset to see who is affected, where they live, when cases rise, and how travel may be linked to cases.

## What is in this repo

| File | Description |
|------|-------------|
| `MalariaImportation.ipynb` | The full analysis notebook, with charts and written findings |

## Dataset

- Clinic records: **3,875 rows, 16 columns**, covering 2022 to 2024.
- Columns include age group, sex, occupation, home district, travel (yes/no), reason for travel, nights away, mainland district visited, and months spent in Zanzibar.
- The data is de-identified (study IDs only).
- **The raw data file is not included in this repo.** Add your own copy and update the file path in the notebook (it currently reads from Google Drive).

## What the notebook does

1. Loads and cleans the data with a `wrangle()` function.
2. Looks at age group, sex, and occupation.
3. Looks at home district of reported cases.
4. Looks at the mainland regions and districts people traveled to.
5. Looks at cases by month to find seasonal patterns.

## Early findings

- About 66% of records are aged 15 to 39.
- About 67% of records are male.
- About 1,100 records list a mainland district that the person traveled to.
- Monthly counts peak around November to January and May to July.

## Limitations

- These results show **association, not cause**. They are consistent with travel playing a role, but do not prove it.
- Months from different years are pooled in the seasonal chart. A year-by-year view is planned.
- Some columns have many missing values (for example, travel details are only filled in for people who traveled).

## How to run

```bash
pip install pandas matplotlib seaborn jupyter
jupyter notebook MalariaImportation.ipynb
```

Open the notebook, change the data file path in the first cells, and run all cells.

## Author

**Nassir Hemed Nassor**
B.Tech, Data Science and AI, IIT Madras Zanzibar

- GitHub: [onlinecitizen](https://github.com/onlinecitizen)
- LinkedIn: [nassir-hemed-nassor](https://www.linkedin.com/in/nassir-hemed-nassor-812b20365)
- Email: nassirnassor021@gmail.com
