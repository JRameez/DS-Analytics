# Redbus Data Scraping with Selenium & Dynamic Filtering using Streamlit

### Overview

This project aims to revolutionize the transportation industry by providing a comprehensive solution for collecting, analyzing, and visualizing bus travel data. Through the use of Selenium for web scraping, this project automates the extraction of detailed information from Redbus, including bus routes, schedules, prices, and seat availability. By streamlining data collection and offering powerful data-driven tools, the project enables improved operational efficiency and strategic decision-making in the transportation sector.

### Approach

Data Scraping:
    Automate the extraction of Redbus data, including routes, schedules, prices, and seat availability using Selenium.

Data Storage:
    Store the scraped data in a SQL database for further processing.

Streamlit Application:

  Develop an interactive Streamlit application to display and filter the scraped data.
  Implement filters for bus type, route, price range, star rating, and seat availability.
  
Data Analysis:

  Use SQL queries to retrieve and filter data based on user inputs.
  Allow users to interact with and filter data through the Streamlit application.

### Necessary Requirements

Before starting, ensure you have the following installed:

Python : A versatile programming language widely used for web scraping, data analysis, and web application development.
ChromeDriver: A separate executable that Selenium WebDriver uses to control Chrome for automating web tasks.
Selenium: A powerful tool for web automation that enables programmatic control of web browsers, crucial for web scraping.
SQL: Any SQL database engine.
Streamlit: A tool for displaying and filtering scraped data in a web interface.

### Installation

I. Selenium
    Selenium enables the automation of web browsers for tasks like web scraping and testing.

   1. Setup Selenium:

        Install the Selenium package:

            pip install selenium
   2.Download and set up the appropriate browser drivers (e.g., ChromeDriver). Driver download links.


II. MySQL Workbench
    It is used as the database engine for storing scraped data.

Setup SQL:

    1.Install MySQL Workbench
    Connect to the database and create a table:
    mydb=mysql.connector.connect(
            host="localhost",
            port=port,
            user="username",
            password="password",
            database="dbname",
    )


    cursor = mydb.cursor(buffered=True)

    # Create table
    cursor.execute("""
    CREATE TABLE IF NOT EXISTS busdetail (
        id INT AUTO_INCREMENT PRIMARY KEY,
        busname VARCHAR(255),
        route_name VARCHAR(255),
        bustype VARCHAR(255),
        departing_time VARCHAR(255),
        duration VARCHAR(255),
        reaching_time VARCHAR(255),
        rating FLOAT,
        price DECIMAL(10, 2),
        seats_available INT,
        route_link VARCHAR(255)
    );
    """)

    # Commit and close connection
    mydb.commit()
    mydb.close()


III. Streamlit
  Streamlit allows you to turn Python scripts into interactive web applications.

Install Streamlit:

  pip install streamlit
Example Usage:

  Create a new file called streamlit_app.py with the following code:

  import streamlit as st
  x = st.slider("Select a value")
  st.write(x, "squared is", x * x)
  
Run the application:

  streamlit run streamlit_app.py
  Visit the Streamlit documentation for more details.

## Result

The key objectives of this project include:

  Successfully scraping data from a minimum of 10 government state bus transport services on the Redbus website using         Selenium, alongside private bus data for the selected routes.
  Storing the data in a structured SQL database.
  Developing an interactive and user-friendly Streamlit application for data filtering.
  Ensuring the application delivers a seamless user experience and operates efficiently.

  ## Usage
  
    This solution can be applied in various business scenarios, such as:

  Travel Aggregators: Offering real-time bus schedules and seat availability for customers.
  Market Analysis: Analyzing travel patterns and preferences for market research.
  Customer Service: Enhancing user experience with customized travel options based on data insights.
  Competitor Analysis: Comparing pricing and service levels with competitors.

## References

https://www.selenium.dev/documentation/webdriver/elements/locators/
https://dev.mysql.com/doc/
https://docs.streamlit.io/
