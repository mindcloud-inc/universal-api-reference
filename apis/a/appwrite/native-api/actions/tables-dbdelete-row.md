# Delete row with Appwrite

Deletes the row from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete row](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `rowId` | path | `string` | yes | Row ID. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
