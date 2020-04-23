    #     ___  ____     _    ____ _     _____
    #    / _ \|  _ \   / \  / ___| |   | ____|
    #   | | | | |_) | / _ \| |   | |   |  _|
    #   | |_| |  _ < / ___ | |___| |___| |___
    #    \___/|_| \_/_/   \_\____|_____|_____|
***

# OCI Data Catalog

Oracle Cloud Infrastructure Data Catalog is an metadata platform that helps you on manage metadata on many silos of data.

In this cloud service, we can manage diffents silos and discover data using an organized inventory of data assets across your cloud account.

With this self-service solution, data consumers can easily find, understand, govern, and track Oracle Cloud data assets.

1. Before Instantiate Data Catalog
   You need to give the right permissions to your cloud tenant. You can check [here](https://docs.cloud.oracle.com/en-us/iaas/data-catalog/using/policies.htm#policies "Oracle Official Documentation").

   To create a policy, please go to menu -> identity -> policy

   In terms of tests, we will give all permission to tenancy

   >> allow service datacatalog to read object-family in tenancy

2. Create Data Catalog
   To instantiate a data catalog service, you should go to menu -> Data and AI -> Data Catalog.

   Choose your prefered compartment and click in "Create Data Catalog".
   ![Creating Data Catalog!](create_data_catalog.png "Data catalog service")

3. j

Link:

[Policies] https://docs.cloud.oracle.com/en-us/iaas/data-catalog/using/policies.htm#policies
https://aws.amazon.com/quicksight/
https://docs.cloud.oracle.com/en-us/iaas/data-catalog/tutorials/harvest-object-storage.htm
