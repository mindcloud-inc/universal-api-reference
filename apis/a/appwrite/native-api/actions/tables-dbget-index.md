# Get index with Appwrite

Retrieves the index from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/indexes/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get index](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | path | `string` | yes | Index Key. |
