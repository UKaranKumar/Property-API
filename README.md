# Property-API

Title of project - Property details

Ngrok url: http://c117-35-227-67-78.ngrok.io/

As the task assigned I analyzed a dataset of real estate properties and created an API to expose the results, here's a step-by-step guide on how I approached the task.

**Section 1: Environment Setup and Data Cleaning**

In this section, the goal was to prepare the dataset for analysis. Here's what I did:

1. **Environment Setup**: I started by setting up my environment in Google Colab. I imported the necessary libraries such as NumPy, Pandas, and SQLite to work with the data.

2. **Data Loading**: I loaded the dataset from a CSV file using Pandas, creating a DataFrame to work with.

3. **Data Cleaning**:
   - Removed unnecessary columns (e.g., 'ad_type', 'title', 'description', 'l4', 'l5', 'l6') from the DataFrame as they were not needed for analysis.
   - Removed rows with missing values in critical columns (e.g., 'lon', 'lat', 'price_period', 'bedrooms', 'surface_total', 'rooms', 'price', 'surface_covered').

4. **Database Setup**: I created two separate tables, 'Property_Details' and 'Property_Price_Details,' and loaded the cleaned data into an SQLite database for further analysis.

**Section 2: Data Analysis**

In this section, I performed various data analyses as per the provided questions. Here's a summary of each analysis:

1. Retrieved properties with a price greater than 1 million located in "Estados Unidos."
2. Categorized properties into 'Small,' 'Medium,' or 'Large' based on their surface area.
3. Listed all properties in the "Belgrano" neighborhood with the same number of bedrooms and bathrooms as others.
4. Calculated the average price per square meter for each property type in the "Belgrano" neighborhood.
5. Identified properties with a higher price than the average price of properties with the same number of bedrooms and bathrooms.
6. Calculated cumulative prices for each property type, ordered by creation date.
7. Identified the top 10 locations with the highest total surface area of properties listed for sale.
8. Found the top 5 most expensive properties in the "Palermo" neighborhood listed in August 2020.
9. Listed the top 3 properties with the highest price per square meter within each property type.
10. Identified the top 3 locations with the highest average price per square meter for properties listed for sale in the year 2020, excluding locations with fewer than 10 properties.

**Section 3: Exposing the Results in an API**

In this section, I created a Flask API to expose the results of the data analysis. Here are the key steps:

1. Set up a Flask server in the Collab notebook.
2. Created API endpoints for each of the 10 questions from Section 2.
3. Implemented the GET HTTP method for each endpoint to return the results.
4. Handled basic error cases, such as an invalid question number.

I also set up ngrok to create an HTTP share of the notebook, allowing you to access the API via a public URL.

Overall, this README summarizes the process of cleaning the data, conducting data analysis, and creating an API to expose the results of the analysis in a clear and organized manner. The code provided in the Collab notebook implements these steps.

