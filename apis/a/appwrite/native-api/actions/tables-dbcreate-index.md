# Create index with Appwrite

Creates a new index in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/indexes`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create index](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Array of columns to index. Maximum of 100 columns are allowed, each 32 characters long. |
| `databaseId` | path | `string` | yes | Database ID. |
| `lengths` | body | `string` | no | Length of index. Maximum of 100 |
| `orders` | body | `string` | no | Array of index orders. Maximum of 100 orders are allowed. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | body | `string` | yes | Index Key. |
| `type` | body | `string` | yes | Index type. |
| `columns[]` | body | `array<string>` | yes | Array of columns to index. Maximum of 100 columns are allowed, each 32 characters long. |
| `orders[]` | body | `array<string>` | no | Array of index orders. Maximum of 100 orders are allowed. |
| `lengths[]` | body | `array<number>` | no | Length of index. Maximum of 100 |
