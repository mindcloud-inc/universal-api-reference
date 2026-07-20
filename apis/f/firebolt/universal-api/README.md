# <img src="https://images.mindcloud.co/apps/icons/firebolt_1776877497331.png" alt="Firebolt logo" width="28" height="28"> Firebolt: Universal API

Run Firebolt queries and manage engines

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/firebolt/latest
- **Category:** Business Intelligence / Data Warehouse
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.firebolt.io/
- **Vendor API docs:** https://docs.firebolt.io/guides/developing-with-firebolt/using-the-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get System Engine URL](actions/get-system-engine-url.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/get-system-engine-url?connectionId=$CONNECTION_ID&accountName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Async Query Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Async Query Status](actions/check-async-query-status.md) | GET | Retrieves asynchronous query status from Firebolt. |

### Async Sql Query

| Action | Method | Description |
| --- | --- | --- |
| [Run Async SQL Query](actions/run-async-sql-query.md) | POST | Creates an asynchronous SQL query in Firebolt. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [List Columns](actions/list-columns.md) | GET | Retrieves columns from Firebolt. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a new database in Firebolt. |
| [List Databases](actions/list-databases.md) | GET | Retrieves databases from Firebolt. |
| [Update Database](actions/update-database.md) | PUT | Updates an existing database in Firebolt. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in Firebolt. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Engine](actions/create-engine.md) | POST | Creates a new engine in Firebolt. |
| [Describe Object](actions/describe-object.md) | GET | Retrieves object details from Firebolt. |
| [Get Engine Metrics History](actions/get-engine-metrics-history.md) | GET | Retrieves engine metrics history from Firebolt. |
| [Get Engine Query History](actions/get-engine-query-history.md) | GET | Retrieves engine query history from Firebolt. |
| [Get Storage History](actions/get-storage-history.md) | GET | Retrieves storage history from Firebolt. |
| [List Engines](actions/list-engines.md) | GET | Retrieves engines from Firebolt. |
| [List Indexes](actions/list-indexes.md) | GET | Retrieves indexes from Firebolt. |
| [List Running Queries](actions/list-running-queries.md) | GET | Retrieves running queries from Firebolt. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from Firebolt. |
| [Recommend DDL](actions/recommend-ddl.md) | GET | Retrieves DDL recommendations from Firebolt. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Copy From S3](actions/copy-from-s3.md) | POST | Creates a copy-from-S3 operation in Firebolt. |
| [Copy To S3](actions/copy-to-s3.md) | POST | Creates a copy-to-S3 operation in Firebolt. |
| [Delete Engine](actions/delete-engine.md) | DELETE | Deletes an existing engine from Firebolt. |
| [Delete Rows](actions/delete-rows.md) | DELETE | Deletes existing rows from Firebolt. |
| [Explain Query](actions/explain-query.md) | GET | Retrieves a query plan from Firebolt. |
| [Insert Rows](actions/insert-rows.md) | POST | Creates row inserts in Firebolt. |
| [Merge Rows](actions/merge-rows.md) | POST | Creates row merges in Firebolt. |
| [Start Engine](actions/start-engine.md) | PUT | Starts an engine in Firebolt. |
| [Stop Engine](actions/stop-engine.md) | PUT | Stops an engine in Firebolt. |
| [Update Engine](actions/update-engine.md) | PUT | Updates an existing engine in Firebolt. |
| [Update Rows](actions/update-rows.md) | PUT | Updates existing rows in Firebolt. |
| [Vacuum Table](actions/vacuum-table.md) | PUT | Updates table storage in Firebolt with VACUUM. |

### Query

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Query](actions/cancel-query.md) | DELETE | Deletes a running query from Firebolt. |
| [Firebolt Query Helper](actions/firebolt-query-helper.md) | GET | Retrieves query results from Firebolt. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Create Role](actions/create-role.md) | POST | Creates a new role in Firebolt. |
| [Grant Privileges](actions/grant-privileges.md) | POST | Creates privilege grants in Firebolt. |

### Sql Query

| Action | Method | Description |
| --- | --- | --- |
| [Run Sync SQL Query](actions/run-sync-sql-query.md) | GET | Retrieves synchronous query results from Firebolt. |

### System Engine Url

| Action | Method | Description |
| --- | --- | --- |
| [Get System Engine URL](actions/get-system-engine-url.md) | GET | Retrieves a system engine URL from Firebolt. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Firebolt. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Create View](actions/create-view.md) | POST | Creates a new view in Firebolt. |
| [Delete View](actions/delete-view.md) | DELETE | Deletes an existing view from Firebolt. |
| [List Views](actions/list-views.md) | GET | Retrieves views from Firebolt. |

