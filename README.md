# WPRDC-data-API-overview
An overview of the Western Pennsylvania Regional Data Center's data API services

The Western Pennsylvania Regional Data Center's data portal runs on CKAN. CKAN has an API that allows the user to do things like [get a list of all datasets on the WPRDC data portal](https://data.wprdc.org/api/3/action/package_list), get a list of all datasets with resources and dataset metadata, download the data from any data table on the portal, or even run SQL queries.

Click [this link](https://data.wprdc.org/api/3/action/datastore_search_sql?sql=SELECT%20*%20from%20%2237b11f07-361f-442a-966e-fbdc5eef0840%22%20WHERE%20%22DogName%22%20LIKE%20%27MR.%%27) to get a JSON-formatted response with all dogs licensed in Allegheny County whose names start with "MR.".

We've done [a workshop](https://github.com/WPRDC/api-training) on using web APIs in general and the WPRDC's APIs in particular. The linked GitHub repository includes examples and documention on using our data API.

### Documentation
The CKAN API documentation is [here](https://docs.ckan.org/en/2.7/api/index.html). Documenation for the datastore_search and datastore_search_sql endpoints (for querying data tables) are [here](https://docs.ckan.org/en/2.7/maintaining/datastore.html#ckanext.datastore.logic.action.datastore_search) and [here](https://docs.ckan.org/en/2.7/maintaining/datastore.html#ckanext.datastore.logic.action.datastore_search_sql). 

### Some data API examples
#### Making SQL queries on WPRDC Data
- [Jupyter notebook showing how to get and use WPRDC data in Python](https://github.com/WPRDC/Jupyter-notebooks-by-dataset/blob/master/Crash-Data-Analysis.ipynb) - Page down to the "Using SQL queries" section.
#### CKAN API usage under R + debugging a broken SQL query
- [Using the CKAN API wrapper + converting string fields to integers in SQL queries](https://gist.github.com/drw/3fa37a32dcb49d42820347b8b735bec3) - Addressing a common pitfall when running SQL queries, this R script shows how to convert a string field to an integer and then use it in the WHERE clause of a SQL query. This also gives a simple example of using the ckanr wrapper package to more easily use the CKAN API.
#### Tiny CKAN API examples
- [How to build and run very simple datastore queries using Python](https://github.com/WPRDC/api-workshop/blob/master/Tiny_Examples.ipynb) - Again the "datastore" is a database that stores tables of data on the WPRDC data portal (like uploaded CSV files). 

