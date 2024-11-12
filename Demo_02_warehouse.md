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

### 4.create multi-cluster virtual warehouse by SQL
    USE ROLE SYSADMIN;
    CREATE OR REPLACE WAREHOUSE ACCOUNTING_WH
    WITH Warehouse_Size = MEDIUM MIN_CLUSTER_COUNT = 1
    AUTO_SUSPEND = 300 AUTO_RESUME = true INITIALLY_SUSPENDED = true;
    MAX_CLUSTER_COUNT = 6 SCALING_POLICY = 'STANDARD';

