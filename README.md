


# Limitless Analytics with Azure Synapse

<a href="https://www.packtpub.com/product/limitless-analytics-with-azure-synapse/9781800205659"><img src="https://static.packt-cdn.com/products/9781800205659/cover/smaller" alt="Book Name" height="256px" align="right"></a>

This is the code repository for [Limitless Analytics with Azure Synapse](https://www.packtpub.com/product/limitless-analytics-with-azure-synapse/9781800205659), published by Packt.

**An end-to-end analytics service for data processing, management, and ingestion for BI and ML requirements**

## What is this book about?
Azure Synapse Analytics, which Microsoft describes as the next evolution of Azure SQL Data Warehouse, is a limitless analytics service that brings enterprise data warehousing and big data analytics together. With this book, you'll learn how to discover insights from your data effectively using this platform.

This book covers the following exciting features: 
* Explore the necessary considerations for data ingestion and orchestration while building analytical pipelines
* Understand pipelines and activities in Synapse pipelines and use them to construct end-to-end data-driven workflows
* Query data using various coding languages on Azure Synapse
* Focus on Synapse SQL and Synapse Spark
* Manage and monitor resource utilization and query activity in Azure Synapse
* Connect Power BI workspaces with Azure Synapse and create or modify reports directly from Synapse Studio

If you feel this book is for you, get your [copy](https://www.amazon.com/Limitless-Analytics-Azure-Synapse-end/dp/1800205651) today!

<a href="https://www.packtpub.com/?utm_source=github&utm_medium=banner&utm_campaign=GitHubBanner"><img src="https://raw.githubusercontent.com/PacktPublishing/GitHub/master/GitHub.png" alt="https://www.packtpub.com/" border="5" /></a>

## Instructions and Navigations
All of the code is organized into folders. For example, Chapter06.

The code will look like the following:
```
DROP VIEW IF EXISTS populationView;
GO

CREATE VIEW populationView AS
SELECT * 
FROM OPENROWSET(
        BULK 'csv/population/population.csv',
        DATA_SOURCE = 'SqlOnDemandDemo',
        FORMAT = 'CSV', 
        FIELDTERMINATOR =',', 
        ROWTERMINATOR = '\n'
    )
WITH (
    [country_code] VARCHAR (5) COLLATE Latin1_General_BIN2,
    [country_name] VARCHAR (100) COLLATE Latin1_General_BIN2,
    [year] smallint,
    [population] bigint
) AS [r];

```

**Following is what you need for this book:**
This book is for data engineers, IT professionals, business analysts, data scientists, and database administrators who are looking to get up and running with the Azure Synapse Analytics platform. Basic knowledge of data warehousing will be beneficial to help you understand the concepts covered in this book more effectively.

With the following software and hardware list you can run all code files present in the book (Chapter 1-14).

### Software and Hardware List

| Chapter  | Software required                                                                                  | OS required                        |
| -------- | ---------------------------------------------------------------------------------------------------| -----------------------------------|
| 1-14     | Microsoft Azure Account, SQL Server Management Studio, Azure Data Studio, Power BI, Visual Studio  | Windows, Mac OS X, and Linux (Any) |
| 11       | Microsoft Azure Powershell                                                                         | Windows, Mac OS X, and Linux (Any) |


We also provide a PDF file that has color images of the screenshots/diagrams used in this book. [Click here to download it](https://static.packt-cdn.com/downloads/9781800205659_ColorImages.pdf).

### Related products <Other books you may enjoy>
* Azure Data Factory Cookbook[[Packt]](https://www.packtpub.com/product/azure-data-factory-cookbook/9781800565296) [[Amazon]](https://www.amazon.com/Azure-Data-Factory-Cookbook-integration/dp/1800565291)

* Azure Data Engineering Cookbook [[Packt]](https://www.packtpub.com/product/azure-data-engineering-cookbook/9781800206557) [[Amazon]](https://www.amazon.com/Azure-Data-Engineering-Cookbook-implement/dp/1800206550)

## Get to Know the Author
**Prashant Kumar Mishra**
is an engineering architect at Microsoft. He has more than 10 years of professional expertise in the Microsoft data and AI segment as a developer, consultant, and architect. He has been focused on Microsoft Azure Cloud technologies for several years now and has helped various customers in their data journey. He prefers to share his knowledge with others to make the data community stronger day by day through his blogs and meetup groups.
### Download a free PDF

 <i>If you have already purchased a print or Kindle version of this book, you can get a DRM-free PDF version at no cost.<br>Simply click on the link to claim your free PDF.</i>
<p align="center"> <a href="https://packt.link/free-ebook/9781800205659">https://packt.link/free-ebook/9781800205659 </a> </p>