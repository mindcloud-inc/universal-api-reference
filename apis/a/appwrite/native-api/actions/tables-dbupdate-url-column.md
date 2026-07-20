# Update URL column with Appwrite

Updates the URL column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/url/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update URL column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | path | `string` | yes | Column Key. |
| `required` | body | `boolean` | yes | Is column required? |
| `default` | body | `string` | yes | Default value for column when not provided. Cannot be set when column is required. |
| `newKey` | body | `string` | no | New Column Key. |
