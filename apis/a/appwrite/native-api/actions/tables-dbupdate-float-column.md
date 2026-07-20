# Update float column with Appwrite

Updates the float column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/float/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update float column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | path | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `min` | body | `number` | no | Minimum value |
| `max` | body | `number` | no | Maximum value |
| `default` | body | `number` | yes | Default value. Cannot be set when required. |
| `newKey` | body | `string` | no | New Column Key. |
