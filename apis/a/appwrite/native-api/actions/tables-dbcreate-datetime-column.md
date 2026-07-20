# Create datetime column with Appwrite

Creates a new datetime column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/datetime`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create datetime column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | body | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | no | Default value for the column in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. Cannot be set when column is required. |
| `array` | body | `boolean` | no | Is column an array? |
