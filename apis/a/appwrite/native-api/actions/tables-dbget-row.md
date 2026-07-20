# Get row with Appwrite

Retrieves the row from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get row](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `rowId` | path | `string` | yes | Row ID. |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. Send multiple values as a array. |
| `transactionId` | query | `string` | no | Transaction ID to read uncommitted changes within the transaction. |
