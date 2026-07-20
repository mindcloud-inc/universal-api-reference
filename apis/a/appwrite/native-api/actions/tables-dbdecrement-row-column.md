# Decrement row column with Appwrite

Decrements the row column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}/{column}/decrement`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Decrement row column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `rowId` | path | `string` | yes | Row ID. |
| `column` | path | `string` | yes | Column key. |
| `value` | body | `number` | no | Value to increment the column by. The value must be a number. |
| `min` | body | `number` | no | Minimum value for the column. If the current value is lesser than this value, an exception will be thrown. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
