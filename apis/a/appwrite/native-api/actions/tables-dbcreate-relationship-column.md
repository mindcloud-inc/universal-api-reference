# Create relationship column with Appwrite

Creates a new relationship column in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/columns/relationship`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create relationship column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `relatedTableId` | body | `string` | yes | Related Table ID. |
| `type` | body | `string` | yes | Relation type |
| `twoWay` | body | `boolean` | no | Is Two Way? |
| `key` | body | `string` | no | Column Key. |
| `twoWayKey` | body | `string` | no | Two Way Column Key. |
| `onDelete` | body | `string` | no | Constraints option |
