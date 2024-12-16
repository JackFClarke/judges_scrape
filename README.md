# README: Scrape.ipynb

## Overview

This Jupyter Notebook, `scrape.ipynb`, is designed to extract, process, and visualize data related to the professional backgrounds of individuals appointed to the judiciary. The notebook is structured to facilitate data extraction from a database, process the data for analysis, and generate visual representations to aid in understanding the distribution of various professional backgrounds.

## Workflow

1. **Data Extraction:**
   - The notebook begins by connecting to a database named `judges3.db` to retrieve information about partners who have worked before judges. This is achieved using a function `get_partners_before_judges`, which queries the database and returns a list of tuples containing the name, firm, and years of service for each partner.

2. **Data Display:**
   - The extracted data is printed in a formatted manner to provide a quick overview of the partners' details, including their names, firms, and years of service.

3. **Data Visualization:**
   - A pie chart is created using `matplotlib` to visualize the distribution of different professional backgrounds among appointed individuals in the judiciary. The chart categorizes backgrounds into sectors such as Big Law, Federal Prosecution, Public Defense, and others, with corresponding percentages and color coding for clarity.

4. **Output:**
   - The notebook outputs a pie chart titled "Backgrounds of Appointed Individuals in the Judiciary," which provides a visual summary of the data, highlighting the proportion of individuals from each professional background.

## Usage

- Ensure that the `judges3.db` database is accessible and contains the necessary data.
- Run the notebook cells sequentially to extract, process, and visualize the data.
- The pie chart generated at the end of the notebook offers insights into the professional diversity of the judiciary appointees.

## Dependencies

- Python 3.x
- Jupyter Notebook
- SQLite3 (for database interaction)
- Matplotlib (for data visualization)
