# Create string column with Appwrite

Creates a new string column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/string`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create string column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). |
| `key` | body | `string` | yes | Column Key. |
| `size` | body | `number` | yes | Column size for text columns, in number of characters. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | no | Default value for column when not provided. Cannot be set when column is required. |
| `array` | body | `boolean` | no | Is column an array? |
| `encrypt` | body | `boolean` | no | Toggle encryption for the column. Encryption enhances security by not storing any plain text values in the database. However, encrypted columns cannot be queried. |
