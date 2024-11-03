### 1.create virtual warehouse by Web UI snowsight
* Name:TEST1_WH
* Size:Small
* Multi-cluster:1-3
* Mode:auto-scale
* Scaling Policy:Standard

### 2.create virtual warehouse by SQL
   USE ROLE SYSADMIN;
   CREATE WAREHOUSE TEST2_WH WITH WAREHOUSE_SIZE = MEDIUM
   AUTO_SUSPEND = 300 AUTO_RESUME = true INITIALLY_SUSPENDED = true;

### 3.alter virtual warehouse by SQL
   USE ROLE SYSADMIN;
   ALTER WAREHOUSE TEST2_WH SET WAREHOUSE_SIZE = LARGE;



### 2.menu introduction
### 3.user profile introduction
### 4.worksheets introduction
#### features:
* charts
* dashboards
* collaboration
* Improved Productivity
    * auto-save
    * history
    * auto complete
    * formatting SQL
#### context setting:
* virtual warehouse
* role
* database
* schema
### 5.create folder
Name:Demo
### 6.create worksheet
Name:demo_01_snowsight
### 7.create query sample
    SELECT CURRENT_WAREHOUSE() as WH, CURRENT_ROLE() AS ROLE, CURRENT_DATABASE() AS DB;
### 8.query statement block
    USE DATABASE SNOWFLAKE_SAMPLE_DATA;
    SELECT CURRENT_WAREHOUSE() as WH, CURRENT_ROLE() AS ROLE, CURRENT_DATABASE() AS DB;

