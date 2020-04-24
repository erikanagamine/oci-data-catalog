    #     ___  ____     _    ____ _     _____
    #    / _ \|  _ \   / \  / ___| |   | ____|
    #   | | | | |_) | / _ \| |   | |   |  _|
    #   | |_| |  _ < / ___ | |___| |___| |___
    #    \___/|_| \_/_/   \_\____|_____|_____|
***

# OCI Data Catalog

Oracle Cloud Infrastructure Data Catalog is a metadata platform that helps you on manage metadata on many silos of data.

In this cloud service, we can manage diffents silos and discover data using an organized inventory of data assets across your cloud account.

With this self-service solution, data consumers can easily find, understand, govern, and track Oracle Cloud data assets.

# 1. Before Instantiate Data Catalog
   You need to give the right permissions to your cloud tenant. You can check [here](https://docs.cloud.oracle.com/en-us/iaas/data-catalog/using/policies.htm#policies "Oracle Official Documentation").

   To create a policy, please go to menu -> identity -> policy

   In terms of tests, we will give all permission to tenancy, but as a best practice, you should check the right permission:
   
   >> allow service datacatalog to read object-family in tenancy


# 2. Create Data Catalog
   To instantiate a data catalog service, you should go to menu -> Data and AI -> Data Catalog.

   Choose your prefered compartment and click in "Create Data Catalog".

   ![Creating Data Catalog!](create_data_catalog.png "Data catalog service")

   On the creation screen, you need to choose the compartment and the name of this service and click in "Create Data Catalog".
   
   ![Creating Data Catalog!](create_data_catalog_screen.png "Data catalog service")

   PS. You can add a tag on the service if you want to create a budget segregated report.

   After creating your service, you should click the service created on the page:

   ![Creating Data Catalog!](catalog_service.png "Data catalog service")

# 3. Navigate into the console
   
   After access the main page of Data Catalog service, you can check your assets by type or tags.

   ![Data Catalog!](catalog_service-main_page.png "Data catalog service - Main page")

   At this moment you need to create

# 4. Create a new asset

To harvest your data source, you need to register your data source as a data asset in your data catalog instance. A data asset is any physical data store or stream of data such as a database, a cloud storage container, or a message stream.

To create a data asset, you need to specify data source details required to register your data source. The details differ depending on the data source you use to create your data asset. You create a data asset from a wide range of supported data sources.

Here's how you create a data asset:

- On your data catalog instance Home tab, click Create Data Asset from the Quick Actions tile. You can also click Create Data Asset on the Data Assets tab.
- In the Create Data Asset panel, enter a Name to uniquely identify your data asset. You may edit the name later.
- Optionally, enter a Description to specify the need or purpose for creating this data asset. Both Description and Name are searchable fields in the Data Catalog.
- From the Type drop-down list, select the type of data asset you want to create. Additional fields display, depending on what you choose. Use the following table to complete the additional fields.

## Supported Data Sources
You use the following Oracle Cloud Infrastructure data sources to create data assets in :

- Object Storage
- Oracle Database
- MySQL
- Apache Hive installed on Oracle Cloud Infrastructure
- Kafka streams installed on Oracle Cloud Infrastructure

Depending on the type of data asset you create, you use different data structures to browse the data entities. For example, if you create an Oracle Database data asset, you browse through database objects to review the table and view data entities.

## Supported File Types
The following file types are supported for Oracle Object Storage:

- Comma Separated Value (CSV) files (.csv, .csv.gv)
- XML files (.xml, .xsd)
- AVRO files (.avro, .avro.gz)
- Excel files (.xls, .xlsx)
- Apache Parquet files (.parquet, .pq)
- Apache ORC files (.orc)
- Simple JSON files (.json, .json.gz)

## What are Data Entities and Attributes
A data asset contains one or more data entities. A data entity is a collection of data such as a database table or view, or a single logical file. A data entity normally has many attributes that describe its data. An attribute describes a data item with a name and data type.

|Data Asset |	Data Entities	|Attributes|
|----------|------------------|----------|
|Database	|Tables and Views	| Columns|
|File | Container	Files | Fields|
|Data |Stream	Event or Topic or Payload |	Keys|



# 5. Harvesting

When you harvest a data asset, the harvester extracts, standardizes, and indexes metadata information from the data asset to create a unified and searchable repository in the data catalog. You then browse or explore the data catalog to view the harvested data entities and attributes to annotate and enrich the data assets.

Harvesting a data source involves the following steps:

- Identify connectivity details to connect to the data source.
- Create a data asset.
- Add a connection to your data asset.
- Harvest the data asset.

[More information - Oracle Documentation](https://docs.cloud.oracle.com/en-us/iaas/data-catalog/using/harvest-technical-metadata.htm#harvest "Oracle Official Documentation").

# 6. Create a glossary

You use a business glossary to define your concepts across your business domain. Creating a business glossary brings common understanding of the vocabulary used throughout your organization. In Data Catalog, you create categories and terms in a glossary to manage and organize your business concepts.

 # Accessing the Create Glossary Panel
You access the Create Glossary panel, from the Home tab or the Glossaries tab.

- On the Home tab, click Create Glossary in the Quick Actions tile. The Create Glossary panel opens as an overlay.
- On the Glossaries tab, click Create Glossary. You access the Glossaries tab by clicking Glossaries on the Home tab or by clicking + from tabs and selecting Glossaries.

# Creating a Glossary
Here's how you create a glossary:

- Access the create glossary panel.
- In the Name field, enter a unique name for the glossary.
- Optionally, in the Description field, specify the purpose of creating this glossary.
- Click Save.

The glossary is created and the glossary details tab displays.

After creating the glossary, you can configure the glossary by creating categories and terms and creating links to data objects and links within terms.

# Creating a Category
In a glossary, each term must be created within a category.

Here's how you create a category:

- On the glossary details tab of the glossary where you want to create a category, click Create Category.
- In the Create Category panel, enter a Name and Definition for the category.
- Click Save.
- The category is created and the category is seen in the glossary details tab.

After the category is created, it is listed in the Hierarchy pane of the glossary details tab and you can create terms within this category. You can also create a category within another category creating nested categories.

# Creating a Term
You use terms to classify the harvested data entities and attributes. Each term must be created within a category.

Here's how you create a Term:

- Access the glossary details tab of the glossary where you want to create a term.
- In the Hierarchy pane of the glossary details tab, click the category where you want to create a term.
- Click Create Term.
- In the Create Term panel, enter a Name and Definition for the term. A term name must be unique within its category.
- Click Save.

The term is created and the term displays in the glossary details tab.



# Links:

- [Official documentation](https://docs.cloud.oracle.com/en-us/iaas/data-catalog/using/policies.htm#policies "Oracle Official Documentation").
  
- [White paper](https://www.oracle.com/a/ocom/docs/oci-data-catalog-data-sheet.pdf "Oracle Official Documentation").

- [Official Blog](https://blogs.oracle.com/bigdata/what-is-oracle-cloud-infrastructure-data-catalog  "Oracle Blog").
