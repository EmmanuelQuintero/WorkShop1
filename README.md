# Workshop 1 Python Data Engineer

# Overview
Welcome!
This project is based on the creation of a Python application that manages and visualizes data from candidates who participated in selection processes. A CSV file is provided with random data about the candidates, and the goal is to migrate this data to a relational database, perform analysis and manipulations on the data, and then generate visualizations of this data from the database.

# Dataset Information
  - First Name: Object
  - Last Name: Object
  - Email: Object
  - Application Date: Object
  - Country: Object
  - Years Of Experience (YOE) : int64
  - Seniority : Object
  - Technology : Object
  - Code Challenge Score : int64
  - Technical Interview Score : int 64

# Tools used
  - Pyhton
  - Jupyter Notebook
  - PostgresSQL 15
  - SQLAlchemy
  - Pandas
  - Matplotlib
  - Power BI

# Project Features

- Data migration: The data from the CSV file is migrated to a relational database in this case PostgreSQL.
- Exploratory data analysis: EDA performed on the data once migrated to the database to see the data types, some histograms, unique data, and null data
- Identification of hired candidates: Recruitment logic is applied to identify candidates who have been hired.
- Data analysis: Analysis is carried out on the data stored in the database according to criteria such as hiring by technology, year, seniority, country, etc.
- Visualizations: Visualizations are generated in Power BI using graphics such as pie charts, bar charts and multiline charts to represent the results of the analyzes performed.

# Requirements

- Install Python
- Install PostgreSQL
- Install PowerBI

# Database Configuration
To run the application correctly, you need to create a JSON file called `connection.json` to connect to the database in postgresSQL with the following format and fill the values with information from your database:

```json
{
    "host": "your_postgres_host",
    "port": "your_postgres_port",
    "database": "database_name",
    "user": "your_postgres_user",
    "password": "your_postgres_password"
}
```

# To Run this project

1. Clone the project:
```bash
  git clone https://github.com/emmanuelqp/WorkShop1.git)https://github.com/emmanuelqp/WorkShop1.git
```
2. Go to the project directory:
```bash
cd WorkShop1
```
3. Create virtual environment for Python:
```bash
python -m venv venv
```
4. Activate virtual environment:
```bash
.\venv\Scripts\activate
```
5. Install libraries:
```bash
pip install requirements.txt
```
6. Create a database in PostgreSQL
7. The project have an Jupyter Notebook, "workshopy.ipynb" and this notebook is divided into 5 sections :
- I recommend you start with section #1: Import modules and libraries, Connection to PostgreSQL, which is where you will import the libraries and modules that were necessary for the development of the  workshop.
    ##### Note: In the second block of code in section #1 you must change the name of the JSON file to the name of the JSON file that you need to create to be able to make the connection to the database. In my case the name of my file was `connection.json`. If you decide to name your file the same way, remember to change the values specified in the `Database Configuration` field located in the README.
- The second step is to run section 2, which is where the table is created in the database and the csv data is inserted into the table once the table is created in PostgreSQL
- The third step is to run section 3, which is where the exploratory analysis of the data was carried out in order to better understand its structure, dimensions of the table and some histograms.
- The fourth step is to run section 4, which is where the logic was applied to classify the hired candidates in a new column called "Hired", also where the technologies were classified by categories for better analysis, and finally a new one table was created (candidatesHired) in the database to which the data was inserted with the new columns that were created for the analysis.
- The last step is to run section 5. In this section the required graphs are generated with matplotlib. However, if you want to see my dashboard made in Power BI, you can find it at the end of the README.
8. Power BI :

  
8.1 Create a new dashboard.
![image](https://github.com/emmanuelqp/WorkShop1/assets/111546312/5c08f327-7312-4e49-8fb6-fe5982eea0e0)

8.2 Select the option Get/Import data
![image](https://github.com/emmanuelqp/WorkShop1/assets/111546312/ad564305-0ed1-4a68-9aec-d5778baede27)

8.3 Search PostgreSQL Database


![image](https://github.com/emmanuelqp/WorkShop1/assets/111546312/2c0e0800-713c-4773-a9c7-e51d390cddf9)

8.4 Insert your PostgreSQL server and your database name and accept:


![image](https://github.com/emmanuelqp/WorkShop1/assets/111546312/84572a44-9e86-4ef1-b9b8-6336ecacd1c4)

8.5 If you manage to connect to the database the following will appear:


![image](https://github.com/emmanuelqp/WorkShop1/assets/111546312/e6797b4a-a58a-4631-998b-aa6d50e48086)

8.6 Congrats!, you can now select the table you want to work with, you can upload it to the dashboard and make your own dashboard

# My Dashboard
[My Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYTdjYmRjY2UtODQ2OS00M2FkLThiYmQtNGMzNDAzNGUyMDFlIiwidCI6IjY5M2NiZWEwLTRlZjktNDI1NC04OTc3LTc2ZTA1Y2I1ZjU1NiIsImMiOjR9)

## Project Author
Made and presented by: Emmanuel Quintero

