# Create integer column with Appwrite

Creates a new integer column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/integer`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create integer column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | body | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `min` | body | `number` | no | Minimum value |
| `max` | body | `number` | no | Maximum value |
| `default` | body | `number` | no | Default value. Cannot be set when column is required. |
| `array` | body | `boolean` | no | Is column an array? |
