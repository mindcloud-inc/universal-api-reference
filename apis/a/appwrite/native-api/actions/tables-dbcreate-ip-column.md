# Create IP address column with Appwrite

Creates a new IP address column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/ip`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create IP address column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | body | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | no | Default value. Cannot be set when column is required. |
| `array` | body | `boolean` | no | Is column an array? |
