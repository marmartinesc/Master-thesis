# Master-thesis
The files uploaded in this file contain the thesis document, the dataset created, the map generated and code used during the development on my Master Thesis on the "Exploratory Data Analysis of the Handelsregister to Estimate the Energy Consumption of Germany's Industry Sectors", which . Moreover, there is a Database attached containing the result of the data analysis, as well as a .html file with a map to visualize the results from the dataset.

# Dataset (Master_Thesis_Maria.db)
The final database in SQLite format is constructed by integrating information from three primary sources: the Handelsregister (Commercial Register) and two publicly available energy consumption databases. This combination provides a comprehensive view of energy-intensive industries. 

To handle the data of the Handelsregister, a public Sqlite database licensed by Creative Commons Attribution License 4.0 and generated by OffenerRegister.de was used, which can be accessed to following this link: https://offeneregister.de/#download .

Moreover, to ellaborate this dataset, two databases were used as reference. These are:
- Fraunhofer's dataset, licensed by CC BY 4.0: Following the link https://isi.pages.fraunhofer.de/pshp/, there is access to the dataset and the paper where the methodology and conclusions are explained.
- Heat recovery potential dataset, licensed by CC BY 4.0: the data can be accessed to following the link: https://s-eenergies-open-data-euf.hub.arcgis.com/search?categories=%252Fcategories%252Fd5.1

The details of the information contained in the dataset are herunder explained:
-*Basic data*: Found un columns 'Name', 'Address', 'Latitude', 'Longitude', 'Register_identifier' and 'Postal_Code'. 
-*Financial data*: 'Stammkapital' for GmbH companies, 'Grundkapital' for AG companies and Hafteinlage for KG companies.
-'Hydrogen potential': Hydrogen potential in Tera Watts hour associated to the companies extracted from the Fraunhofer's database.
-'Distributed Hydrogen Potential TWh': Hydrogen potential assigned with the methodology used to deal with duplicate matches when comparing data sources.
-'Subsector_Name': Ssubsector associated to the companies extracted from the Fraunhofer's database.
-'level_1_Tj', 'level_2_Tj' and 'level_3_Tj','level_1_r_Tj', 'level_2_r_Tj' and 'level_3_r_Tj': Heat recovery potential in Tera Joules associated to the companies when matching them with the heat recovery potential database when using as reference temperature 25°C, 55°C and 95°C for levels 1, 2 and 3 respectively and the value assigned with the methodology used during the methodology.

# Map (Map_Representing_Capital_of_Energy_Intensive_Industries_Germany.html)
In order to visualize the results and be able to locate the companies addressed in the database easily, an interactive map was generated and attached to the GitHub repository associated to this thesis \cite{githubmasterthesis}. The colour of the dots of the map are associated to the sector the company belongs to, something which can be seen in the legend. Some of the sectors encapsulate multiple subsectors, for the following cases: the mineral industry sector includes non-metallic minerals and mineral processing subsectors, and the metal industry sector includes iron and steel, metal processing, non-ferrous metals and steel, primary subsectors. Moreover, the size of the dot indicates the magnitude of the capital, thus providing a graphic overview of the information obtained. 
Whenever the cursor is placed over a dot, a label with the name, sector, capital, hydrogen potential and heat recovery potential is shown.

# Use_of_Heat_Recovery_Potential_Reference_Database.ipynb and Use_of_Hydroge_Potential_Reference_Database.ipynb
Code used to find energy intensive industries from the reference databases (Hydrogen and Heat recovery potential databases) in the Handelsregister registered companies.

# XML_files_download_ with_Selenium.ipynb
Code used to download XML files with structured information of companies in the Handelsregister

# Geocoding_addresses.ipynb
Code used to find coordinates from the addresses in the data sources used.

# lots_validation_H2potential.ipynb and Plots_validation_Heat_level3.ipynb
Code used to create the plots for evaluating the correlation between financial data and energy consumption.

# Generating_final_dataset-ipynb
Code to create final dataset from the datasets created in Use_of_Heat_Recovery_Potential_Reference_Database.ipynb and Use_of_Hydroge_Potential_Reference_Database.ipynb
