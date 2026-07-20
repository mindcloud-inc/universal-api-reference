# Delete rows with Appwrite

Deletes rows from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete rows](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `queries` | body | `string` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `queries[]` | body | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
