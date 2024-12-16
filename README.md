# Judge Data Scraper & Transformer

**Judge Data Scraper & Transformer** notebook. This project scrapes Wikipedia pages of judges, extracting key information, and transforming it into a structured format for analysis. It's inspired by the OpenAI Cookbook on Data Extraction and Transformation.

---

## What Does This Notebook Do?

1. **Scrape Wikipedia Pages:**  
   We started by getting all the links from a wikipedia page of Biden's appointed judges, I only grabbed 185 but that was good enough for this quick project. Using `BeautifulSoup`, we extract the main content up to the "References" section for each of the links to Judge's individual wiki pages.

3. **Extract Insights:**  
   With the help of OpenAI's `GPT-4o`, we extract structured insights from the scraped text. The AI organizes the data into thematic groups and outputs it as a JSON object.

4. **Save Data:**  
   The extracted data is saved into JSON Lines files, one for each judge, in a `results` directory. I did this to easily keep track of the process because each of the AI runs was going to be 20 minutes +

5. **Merge Data:**  
   All those individual JSON Lines files are merged into a single file for easier handling.

6. **Transform Data:**  
   We transform the raw JSON data to fit a predefined schema using `GPT-4o`. All I did was feed chatgpt a few samples of the data I was able to extract and had it conjure up a reference schema that fit the data as much as possible.

7. **Load into SQLite:**  
   The transformed data is loaded into an SQLite database, with tables set up for personal details, education, career, and more.

8. **Query the Database:**  
   Finally, we run some SQL queries to find interesting patterns, like roles before 2021 or judges who were partners before their judicial appointments.

---

## How to Use

1. **Run the Notebook:**  
   Just execute the cells in order. Make sure you have all the necessary libraries installed (`bs4`, `requests`, `openai`, `jsonlines`, `sqlite3`).

2. **Check the Results:**  
   The transformed data will be in the `transformed` directory, and the SQLite database will be named `judges3.db`.

---

## Credits

Big thanks to the OpenAI Cookbook for the inspiration and guidance on data extraction and transformation using `GPT-4o`.

---
