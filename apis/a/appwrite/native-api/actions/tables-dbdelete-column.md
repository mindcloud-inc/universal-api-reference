# Delete column with Appwrite

Deletes the column from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | path | `string` | yes | Column Key. |
