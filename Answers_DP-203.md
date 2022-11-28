# Respuestas Examen DP-203
## Topic 1
1. [ManagerEmployeeKey] [int] NULL 
- [smallint] not available
2. an error
- CREATE TABLE mytestdb.myParquetTable, but SELECT ... FROM mytestdbo.dbo.myParquetTable is different
3. Activities (D-A-C):
   1. Create an empty table named SalesFact_Work that has the same schema as SalesFact
   2. Switch the partition containing the stale data from SalesFact to SalesFact_Work
   3. Drop the SalesFact_Work table
4. File1.csv and File4.csv only
- In Serverless SQL pool requires path/** to return files recursively
- In Hadoop is not necessary
5. Selected:
   1. Parquet: column-oriented binary file format
   2. AVRO: row based format, and has logical type timestamp
6. /{SubjectArea}/{DataSource}/{YYYY}/{MM}/{DD}/{FileData}_{YYYY}_{MM}_{DD}.csv
7. Selected:
   1. Parquet
   2. Avro
8. Selected:
   1. Copy behavior: Merge files
   2. Sink file type: Parquet
9. Selected:
   1.  Dim_Customer: Replicated
   2.  Dim_Employee: Replicated
   3.  Dim_Time: Replicated
   4.  Fact_DailyBookings: Hash distributed
10. Selected:
    1.  Move to cool storage
    2.  Move to archive storage 
11. Selected:
    1.  DISTRIBUTION
    2.  PARTITION
12. As a type 2 slowly changing dimension (SCD) table
13. Order:
    1.  Create a managed identity
    2.  Add the managed identity to the Sales group
    3.  Use the managed identity as the credentials for the data load process
14. Selected:
    1.  User2: 0
    2.  User1: the values stored in the database
15. C
> Only allowed CREATE and DROP
16. Selected:
    1.  Binary or Parquet?
    2.  PreserveHierarchy
17. Geo-redundant storage (GRS)
18. Zone-redundant storage (ZRS)
19. Selected:
    1.  Distribution: Hash
    2.  Indexing: Heap
    3.  Partitioning: None
20. Hash-distributed on PurchaseKey
21. Selected:
    1.  EventCategory: DimEvent
    2.  ChannelGrouping: DimChannel
    3.  TotalEvents: FactEvents
22. Yes, the data copies quickly with compressed
23. No
24. No
25. A materialized view
26. Parquet
27. Azure Databricks
28. Convert the CSV files to Avro
29. Select:
    1.  moved to cool storage
    2.  container1/contoso.csv
30. TransactionMonth
31. Select:
    1.  To minimize storage costs: Store the infraestructure logs in the Cool access tier and the application logs in the Archive access tier.
    2.  To delete logs automatically: Azure Blob Storage lifecycle management rules.
32. Parquet
33. Switch the first partition from stg.Sales to dbo.Sales
34. Select:
    1.  Surrogate primary key
    2.  Effective start date
    3.  Effective end date 
35. Select:
    1.  Transform data for the dimension tables by: Denormalizing to a second normal form
    2.  New IDENTITY columns
36. Select:
    1.  .partitionBy
    2.  ("StoreID","Year","Month","Day","Hour")
    3.  .parquet("/Purchases")
37. 2.4 billion records in 40 partitions    
38. Selected:
    1.  Type 1
    2.  a surrogate key
39. Hash-distributed on PurchaseKey
40. Use OPENROWSET to query the Parquet files
41. Selected:
    - Create an external DATA SOURCE
    - Create an external FILE FORMAT OBJECT
    - Create an external TABLE
42.  Selected:
    - A dimension table for Employee
    - A fact table for Transaction
43. Type 2
44. Selected:
    1.  Create a database scoped credential that uses Azure Active Directory Application and a Service Principal Key
    2.  Create an external data source that uses the abfs location
    3.  Create an external file format and set the `First_Row` option
45. Selected:
    1.  PARTITION
    2.  [TransactionDateID]
46. Only CSV that have file names that beginninh with "tripdata_2020"
47. Selected:
    - SELECT
    - EXPLODE
    - ALIAS
48. Selected:
    1.  Hot
    2.  Cool
    3.  Cool
49. Load the data by using PySpark
50. Create a POOL in workspace1
51. Selected:
    1.  Path pattern: {date}/product.csv
    2.  Date format: YYYY/MM/DD
52. Responses:
    1.  The query combines two streams of partitioned data: YES
    2.  The stream scheme key and count must match the output scheme: YES
    3.  Providing 60 streaming units will optimize the performance of the query: YES
53. Responses:
    1.  CREATE EXTERNAL TABLE
    2.  OPENROWSET
54. Selected:
    1.  blob
    2.  TYPE=HADOOP
55. Parquet
56. Selected:
    1.  HASH
    2.  OrderDateKey
57. Selected:
    1.  Data over five years old: Move to cool storage
    2.  Data over seven years old: Move to archive storage
58. Selected:
    1.  Replication mechanism: Zone-redundant storage (ZRS)
    2.  Failover process: Failover initiated by Microsoft
59. Selected:
    1.  B: CurrentProductCategory
    2.  E: OriginalProductCategory
60. Selected:
    1.  Common.Data: Replicated
    2.  Marketing.WebSessions: Hash
    3.  Staging.WebSessions: Round-robin
61. Selected:
    1.  CLUSTERED COLUMNSTORE INDEX
    2.  `Hash([ProductKey])`
62. Once per year
63. MERGE
64. Apache Parquet
65. YES or NO? (More possible is YES)
66. Replicated (<2GB and dimension table)
67. an IDENTITY column

## Topic 2
1. Select:
    1.  Input type: Stream
    2.  Function: Geospatial
2. Select:
   1. Implement query parallelization by partitioning the data output
   2. Implement query parallelization by partitioning the data input
3. Microsoft.EventGrid
4. Automated
5. Select:
   1. MAX
   2. TumblingWindow
   3. DATEDIFF
6. Pipeline1 and Pipeline2 succeeded
7. Select:
   1. Ingest: Azure Data Factory
   2. Store: Azure Data Lake Storage
   3. Prepare and Train: Azure Databricks
   4. Model and Serve: Azure Synapse Analytics
8. Select: 
   - CASE
   - ELSE
9. Select:
   - OPENROWSET
   - OPENJSON
10. Select:
    - Pivot
    - Cast
11. An annotation
12. Response:
    1.  The Databricks cluster supports multiple concurrent users: YES
    2.  The Databricks cluster minimizes costs when running scheduled jobs that execute notebooks: NO
    3.  The Databricks cluster supports the creation of a Delta Lake Table: YES
13. Azure Databricks
14. Select:
    1.  RIGHT
    2.  20100101,20110101,20120101
15. B, E
16. No. is Tumbling Window
17. No
18. Select:
    1.  DATEDIFF
    2.  LAST
19. Select:
    1.  To the data flow, add a sink transformation to write the rows to a file in blob storage
    2.  To the data flow, add a conditional split transformation to separate the rewos that will cause truncation errors
20. Select:
    1.  dept=='ecommerce', dept=='retail', dept='wholesale'
    2.  disjoint: false
    3.  ecommerce, retail, wholesale, all
21. Order:
    1.  Mount the Data Lake Storage on to DBFS
    2.  Read the file into a data frame
    3.  Perform transformations on the data frame
    4.  Specify a temporary folder to stage the data
    5.  Write the results to a table in Azure Synapse
22. Responses:
    1.  Type: Tumbling window
    2.  Additional properties: `Recurrence: 30 minutes, Start time: 2021-01-01T00:00, Delay: 2 minutes`
23. Responses:
    1.  Azure Event Hub
    2.  Power BI
    3.  Azure Stream Analytics
24. Responses:
    1.  Add a Azure Stream Analytics Custom Deserializer Project (.NET) project ot the solution
    2.  Add .NET deserializer code for Protobuf to the custom deserializer project
    3.  Change the Event Serialization Format to Protobuf in the input.json file of the job and reference the DLL.
25. Azure Integration Runtime
26. Select:
    1.  HubA: Stream
    2.  HubB: Stream
    3.  Database1: Reference
27. `SELECT Country, Count(*) AS Count FROM ClickStream TIMESTAMP BY CreatedAt GROUP BY Country, TumblingWindow(second, 10)`
28. Select:
    1.  LAG
    2.  LIMIT DURATION
29. Event
30. From Azure DevOps, create a release pipeline
31. Azure Blob Storage
32. Hopping
33. Response:
    1.  Service: Azure Stream Analytics
    2.  Window: Tumbling
    3.  Analysis type: Point within polygon
34. ***PREGUNTA DEPRECADA***
35. Response:
    1.  Fail until the node comes back online
    2.  Lowered
36. Upgrade workspace1 to the Premium pricing tier
37. Yes
38. No
39. Hopping
40. Responses:
    1.  ARM templates for the pipeline assets are stored in: adf_publish
    2.  ARM template named `contososales` can be found in: `/dwh_batchetl/adf_publish/contososales`
41. Select:
    1.  TIMESTAMP BY
    2.  TUMBLINGWINDOW
42. Select: 
    1.  Set the partition option to "Dynamic range" (SQL group to ADLS)
    2.  PolyBase (ADLS to SQL group)
43. Select:
    1.  Load methodoloy: Incremental load
    2.  Trigger: Tumbling window
44. No
45. Create a patient (parent?) pipeline that contains the four pipelines and use a schedule trigger
46. Select:
    1.  Create a Database Encryption Key
    2.  Create a Database Scoped Credential
    3.  Create an External Data Source
47. The job lacks the resources to process the volume of incoming data
48. Select:
    1.  TopOne() OVER(PARTITION BY Game ORDER BY Score Desc)
    2.  Hopping(minute, 5)