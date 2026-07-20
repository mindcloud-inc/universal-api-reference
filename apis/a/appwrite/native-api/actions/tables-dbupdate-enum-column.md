# Update enum column with Appwrite

Updates the enum column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/enum/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update enum column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `elements` | body | `string` | no | Updated list of enum values. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | path | `string` | yes | Column Key. |
| `elements[]` | body | `array<string>` | yes | Updated list of enum values. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | yes | Default value for column when not provided. Cannot be set when column is required. |
| `newKey` | body | `string` | no | New Column Key. |
