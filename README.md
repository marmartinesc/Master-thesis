# Master-thesis
The files uploaded in this file contain the code used during the development on my Master Thesis on the "Exploratory Data Analysis of the Handelsregister to Estimate the Energy Consumption of Germany's Industry Sectors". Moreover, there is a Database attached containing the result of the data analysis, as well as a .html file with a map to visualize the results from the dataset.

# Dataset (Dataset_German_Industry.db)
The final database in SQLite format is constructed by integrating information from three primary sources: the Handelsregister (Commercial Register) and two publicly available energy consumption databases. This combination provides a comprehensive view of energy-intensive industries. 

To handle the data of the Handelsregister, a public Sqlite database licensed by Creative Commons Attribution License 4.0 and generated by OffenerRegister.de was used, which can be accessed to following this link: https://offeneregister.de/#download .

Moreover, to ellaborate this dataset, two databases were used as reference. These are:
- Fraunhofer's dataset, licensed by CC BY 4.0: Following the link https://isi.pages.fraunhofer.de/pshp/, there is access to the dataset and the paper where the methodology and conclusions are explained.
- Heat recovery potential dataset, licensed by CC BY 4.0: the data can be accessed to following the link: https://s-eenergies-open-data-euf.hub.arcgis.com/search?categories=%252Fcategories%252Fd5.1

The details of the information contained in the dataset are herunder explained:
-Basic data: Company names, addresses, locations, coordinates. 
-Financial data: Stammkapital, Grundkapital and Hafteinlage
-'Hydrogen potential', 'Distributed Hydrogen Potential TWh' and 'Subsector_Name': hydrogen potential associated to the companies when matching them with the Fraunhofer database and the value assigned with the methodology used during the methodology.
-'level_i' and 'Distributed level_i', 'Eurostat_Name', and 'Distributedlevel_i', 'Distributed: hydrogen potential associated to the companies when matching them with the Fraunhofer database and the value assigned with the methodology used during the methodology.
    

