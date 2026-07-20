# Create boolean column with Appwrite

Creates a new boolean column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/boolean`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create boolean column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | body | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `boolean` | no | Default value for column when not provided. Cannot be set when column is required. |
| `array` | body | `boolean` | no | Is column an array? |
