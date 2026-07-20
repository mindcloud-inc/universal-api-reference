# Create email column with Appwrite

Creates a new email column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create email column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | body | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | no | Default value for column when not provided. Cannot be set when column is required. |
| `array` | body | `boolean` | no | Is column an array? |
