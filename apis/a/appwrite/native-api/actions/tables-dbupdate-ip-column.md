# Update IP address column with Appwrite

Updates the IP address column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/ip/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update IP address column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | path | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | yes | Default value. Cannot be set when column is required. |
| `newKey` | body | `string` | no | New Column Key. |
