
# Amazon Prime Movies and TV Shows Dashboard

## Snapshot of Dashboard (Power BI Service)

![Dashboard_Snapshot](https://app.powerbi.com/view?r=eyJrIjoiN2MzMWVlYWItYzZiYy00NjQxLWFhZDEtOTBkYTYxZGEyODIxIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9)

### Dashboard Link: [Your Power BI Dashboard Link](your_dashboard_link_here)

## Problem Statement

This dashboard provides insights into the Amazon Prime movie and TV show catalog. It helps to analyze various aspects such as content type distribution, ratings, genres, release trends, and geographical distribution. By leveraging these insights, stakeholders can better understand the content library, viewer preferences, and potential gaps in the catalog. Additionally, the dashboard highlights trends in content releases over the years and identifies top countries contributing to Amazon Prime's catalog.

### Steps Followed

- **Step 1:** Loaded the dataset into Power BI Desktop from an Excel file containing Amazon Prime movies and TV shows data.

- **Step 2:** Cleaned and prepared the data using Power Query Editor, ensuring data integrity by checking for empty and erroneous values.

- **Step 3:** In the Report View, I applied a canvas background color of `#19222D` with 0% transparency to create a cohesive and dark-themed visual aesthetic.

- **Step 4:** Created visualizations:
  - **Filled Map:** Displays the total number of shows by country.
    - **Location:** `country`
    - **Tooltips:** Count of distinct `show_id`
    - **Format Settings:** 
      - Map Style: Dark
      - Fill Colors: Conditional formatting using a gradient based on the count of distinct `show_id` with a high value color of `#00A8E1`
      - Background: `#19222D`
      - Border: White with 20 corners
      - Title: White, font size 16, "Total shows by country"
      - Divider: On, white color
  - **Donut Chart:** Shows the distribution of titles between Movies and TV Shows.
    - **Legend:** `type`
    - **Values:** Count of distinct `show_id`
    - **Filters:** Applied to include only Movies and TV Shows
  - **Area Chart:** Illustrates the total number of shows by release year.
    - **X-Axis:** `release_year`
    - **Y-Axis:** Count of distinct `show_id`
    - **Legend:** `type`
  - **Stacked Bar Chart 1:** Shows the distribution of ratings by total Movies and TV Shows.
    - **X-Axis:** Count of distinct `show_id`
    - **Y-Axis:** `rating`
  - **Stacked Bar Chart 2:** Displays the genre distribution across Movies and TV Shows.
    - **X-Axis:** Count of distinct `show_id`
    - **Y-Axis:** `listed_in`

- **Step 5:** Added six cards to display key metrics:
  - **Total Titles:** Represents the total number of titles in the dataset.
    - **Field:** Count of `titles`
  - **Total Ratings:** Shows the total number of ratings available.
    - **Field:** Count of `ratings`
  - **Total Genres:** Displays the total number of genres listed.
    - **Field:** Count of `listed_in`
  - **Total Directors:** Shows the total number of unique directors.
    - **Field:** Count of `directors`
  - **Start Date:** Displays the earliest release year of content in the dataset.
    - **Field:** Minimum of `release_year`
  - **End Date:** Shows the most recent release year of content in the dataset.
    - **Field:** Maximum of `release_year`

- **Step 6:** Published the report to Power BI Service for broader accessibility.

## Insights

The dashboard provides several key insights into Amazon Prime's content catalog:

### [1] Total Shows by Country
   - The filled map shows the distribution of titles by country, highlighting which regions contribute the most content to the platform.

### [2] Titles - Movies and TV Shows
   - The donut chart shows the split between Movies and TV Shows, helping to understand the proportion of different content types available on Amazon Prime.

### [3] Total Shows by Release Year
   - The area chart illustrates the trend in content releases over the years, showing how content production has evolved.

### [4] Ratings by Total Movies and TV Shows
   - The first stacked bar chart reveals the distribution of content across different ratings, which can help identify the most common ratings.

### [5] Genres by Total Movies and TV Shows
   - The second stacked bar chart shows the distribution of content across various genres, giving insight into the diversity of content available.

### [6] Key Metrics
   - **Total Titles:** [9655]
   - **Total Ratings:** [25]
   - **Total Genres:** [519]
   - **Total Directors:** [5771]
   - **Start Date:** [1920]
   - **End Date:** [2021]
