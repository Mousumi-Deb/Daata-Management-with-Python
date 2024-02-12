# Data-Management-with-Python

### COVID-19 Vaccination Data Management and Analysis System

#### Overview:
The COVID-19 Vaccination Data Management and Analysis System is a Python script designed to efficiently handle and analyze COVID-19 vaccination data. Leveraging SQLite as the database management system, this system offers a range of functionalities including database creation, data seeding, data cleaning, querying specific information, and visualizing vaccination trends using Matplotlib.

#### Features:
1. **Database Creation**:
   - The system creates a SQLite database named "vaccination_info.db" with tables structured to store COVID-19 vaccination data in a normalized form.
   
2. **Seeding Database**:
   - Data from a CSV file containing COVID-19 vaccination data can be seamlessly imported into the database using the `seed_database(file_name)` method. This process involves parsing the CSV file, cleaning the data, and inserting it into appropriate tables within the database.

3. **Data Normalization**:
   - The system ensures data integrity and efficiency by normalizing the data across relational tables. Separate tables are created for countries, vaccines, and vaccination information, with foreign key constraints maintaining relational integrity.

4. **Data Cleaning**:
   - The `clean_data()` method allows users to clean the database by deleting all records from the tables. This feature is useful for starting fresh or removing outdated or erroneous data.

5. **Querying Data**:
   - Users can retrieve specific data from the database using methods such as `get_column_data(country_name, column_name, limit)`. This enables tailored analysis, such as examining vaccination trends for particular countries or date ranges.

6. **Visualization**:
   - The system supports visualization of vaccination trends using Matplotlib. Users can generate graphs to visually analyze vaccination trends over time for specific countries, facilitating insightful data exploration.

#### Usage:
1. **Initialization**:
   - Start by creating an instance of the `DataManager` class.
     ```
     data_manager = DataManager()
     ```

2. **Database Creation**:
   - Execute the `create_database()` method to establish the SQLite database and create necessary tables.
     ```
     data_manager.create_database()
     ```

3. **Seeding Database**:
   - Populate the database with data from a CSV file using the `seed_database(file_name)` method.
     ```
     data_manager.seed_database('vaccin_covid.csv')
     ```

4. **Querying Data**:
   - Retrieve specific data from the database using methods like `get_column_data(country_name, column_name, limit)`.
     ```
     data = data_manager.get_column_data('United States', 'total_vaccinations', 10)
     ```

5. **Data Cleaning**:
   - Clean the database by invoking the `clean_data()` method.
     ```
     data_manager.clean_data()
     ```

#### Requirements:
- Python 3.x
- SQLite
- Matplotlib

#### Note:
Ensure that the CSV file containing vaccination data adheres to the required format and is accessible at the specified path before seeding the database. Additionally, make sure to install the necessary dependencies listed above to successfully execute the script.
