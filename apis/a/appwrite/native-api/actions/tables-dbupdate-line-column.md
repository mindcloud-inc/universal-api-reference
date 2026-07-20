# Update line column with Appwrite

Updates the line column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/line/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update line column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `default` | body | `string` | no | Default value for column when not provided, two-dimensional array of coordinate pairs, [[longitude, latitude], [longitude, latitude], …], listing the vertices of the line in order. Cannot be set when column is required. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the TablesDB service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | path | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default[]` | body | `array<string>` | no | Default value for column when not provided, two-dimensional array of coordinate pairs, [[longitude, latitude], [longitude, latitude], …], listing the vertices of the line in order. Cannot be set when column is required. |
| `newKey` | body | `string` | no | New Column Key. |
