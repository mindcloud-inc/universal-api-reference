# Create enum column with Appwrite

Creates a new enum column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/enum`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create enum column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `elements` | body | `string` | no | Array of enum values. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | body | `string` | yes | Column Key. |
| `elements[]` | body | `array<string>` | yes | Array of enum values. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | no | Default value for column when not provided. Cannot be set when column is required. |
| `array` | body | `boolean` | no | Is column an array? |
