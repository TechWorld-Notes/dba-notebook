# Oracle RAC Cluster Operations

This page contains standard operating procedures for managing our 2-node Oracle RAC environments.

## 1. Check Clusterware Status
Run this from the grid user to check the health of the cluster infrastructure across all nodes.

```bash
crsctl check cluster -all

Check Instance and Database Status

```bash

SELECT 
    inst_id, 
    instance_name, 
    host_name, 
    status, 
    database_status 
FROM 
    gv$instance;
