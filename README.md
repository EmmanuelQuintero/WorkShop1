# Workshop 1 Python Data Engineer <img src="https://logos-world.net/wp-content/uploads/2021/10/Python-Symbol.png" alt="Nombre de la Imagen" width="100px"/>
Presented by Emmanuel Quintero

# Overview
Welcome!
This project is based on the creation of a Python application that manages and visualizes data from candidates who participated in selection processes. A CSV file is provided with random data about the candidates, and the goal is to migrate this data to a relational database, perform analysis and manipulations on the data, and then generate visualizations of this data from the database.

# Tools used
  - Pyhton
  - Jupyter Notebook
  - PostgresSQL 15
  - SQLAlchemy
  - Pandas
  - Matplotlib
  - Power BI

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

# Project Features

- Data migration: The data from the CSV file is migrated to a relational database in this case PostgreSQL.
- Exploratory data analysis: EDA performed on the data once migrated to the database to see the data types, some histograms, unique data, and null data
- Identification of hired candidates: Recruitment logic is applied to identify candidates who have been hired.
- Data analysis: Analysis is carried out on the data stored in the database according to criteria such as hiring by technology, year, seniority, country, etc.
- Visualizations: Visualizations are generated in Power BI using graphics such as pie charts, bar charts and multiline charts to represent the results of the analyzes performed.

# About the Repository
The repository has a gitignore, the dataset used, the readme and the jupyter Notebook that was developed to carry out the workshop

# Requirements

- Install Python [Python Downloads](https://www.python.org/downloads/)
- Install PostgreSQL [Postgres Downloads](https://www.postgresql.org/download/)
- Install PowerBI [PowerBI Donwloads](https://www.microsoft.com/en-us/download/details.aspx?id=58494) 

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

1. Clone the project
```bash
  git clone https://github.com/emmanuelqp/WorkShop1.git)https://github.com/emmanuelqp/WorkShop1.git
```
2. Go to the project directory
```bash
cd WorkShop1
```
3. Create virtual environment for Python
```bash
python -m venv venv
```
4. Activate virtual environment
```bash
.\venv\Scripts\activate
```
5. Install libraries
```bash
pip install requirements.txt
```
6. Create a database in PostgreSQL
7. The project have an Jupyter Notebook, "workshopy.ipynb" and this notebook is divided into 5 sections :
    7.1 I recommend you start with section #1: Import modules and libraries, Connection to PostgreSQL, which is where you will import the libraries and modules that were necessary for the development of the  workshop.
    ##### Note: In the second block of code in section #1 you must change the name of the JSON file to the name of the JSON file that you need to create to be able to make the connection to the database. In my case the name of my file was `connection.json`. If you decide to name your file the same way, remember to change the values specified in the `Database Configuration` field located in the README.
    7.2 The second step is to run section 2, which is where the table is created in the database and the csv data is inserted into the table once the table is created in PostgreSQL
    7.3 The third step is to run section 3, which is where the exploratory analysis of the data was carried out in order to better understand its structure, dimensions of the table and some histograms.
    7.4 The fourth step is to run section 4, which is where the logic was applied to classify the hired candidates in a new column called "Hired", also where the technologies were classified by categories for better analysis, and finally a new one table was created (candidatesHired) in the database to which the data was inserted with the new columns that were created for the analysis.
    7.5 The last step is to run section 5. In this section the required graphs are generated with matplotlib. However, if you want to see my dashboard made in Power BI, you can find it at the end of the README.

