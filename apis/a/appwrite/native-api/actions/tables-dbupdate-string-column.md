# Update string column with Appwrite

Updates the string column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/string/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update string column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | path | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | yes | Default value for column when not provided. Cannot be set when column is required. |
| `size` | body | `number` | no | Maximum size of the string column. |
| `newKey` | body | `string` | no | New Column Key. |
