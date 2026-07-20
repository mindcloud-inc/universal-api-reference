# List columns with Appwrite

Retrieves a list of columns from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List columns](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. You may filter on the following columns: key, type, size, required, array, status, error Send multiple values as a array. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
