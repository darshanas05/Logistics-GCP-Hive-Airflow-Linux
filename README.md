# Logistics_GCP_Hive_Airflow_Linux

Greetings!

This project showcases the incremental loading of data from a CSV file into Hive and subsequently moves the processed file to an archived folder.

Tech-Stack Utilized: GCP, Dataproc cluster, Google Storage, Hive, Airflow, Linux.

**Explanation:**

**Dependency Module Import:** We begin by importing all necessary dependency modules.

**Default Airflow Parameters:** Set default parameters for Airflow in default_args.

**DAG Configuration:** Define the DAG description along with parameters such as start date and interval for job execution.

**GCP Configuration:** Specify the GCP project, cluster name, and region. Initialize Hive to create a database for operations.

**Table Creation:** Establish a temporary external table using SQL statements in Hive for initial data loading, as direct loading into partitioned Hive tables from files isn't feasible.

**Partitioned Table Creation:** Utilize SQL statements for the creation of a Hive partitioned table.

**Dynamic Partitioning:** Set partition type to dynamic and load data from the external table into the partitioned table.

**File Archival:** Employ the BashOperator to execute Linux commands, facilitating the movement of processed CSV files to an archived location.

**Execution Order:** Establish the sequence in which all commands are to be executed.
