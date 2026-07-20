# Update relationship column with Appwrite

Updates the relationship column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/{key}/relationship`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update relationship column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `key` | path | `string` | yes | Column Key. |
| `onDelete` | body | `string` | no | Constraints option |
| `newKey` | body | `string` | no | New Column Key. |
