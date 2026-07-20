# List DBMS Connections with SqlBak

Retrieves DBMS connections from SqlBak.

## Endpoint

- **Method:** `GET`
- **Path:** `/dbms_connections`
- **Base URL:** `https://sqlbak.com/public-api/v1`
- **Official documentation:** [List DBMS Connections](https://sqlbak.docs.apiary.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server_id` | query | `number` | no | Filter DBMS connections by server ID. |
| `dbms_type` | query | `list` | no | Filter DBMS connections by DBMS type. Accepted values: `mongodb`, `mysql`, `mysql_phpmyadmin`, `mysql_xtrabackup`, `postgresql`, `sql_server_amazon`, `sql_server_azure`, `sql_server_local`, `sql_server_remote`. |
