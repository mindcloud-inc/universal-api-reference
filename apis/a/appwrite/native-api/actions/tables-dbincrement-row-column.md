# Increment row column with Appwrite

Increments the row column in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}/{column}/increment`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Increment row column](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `tableId` | path | `string` | yes | Table ID. |
| `rowId` | path | `string` | yes | Row ID. |
| `column` | path | `string` | yes | Column key. |
| `value` | body | `number` | no | Value to increment the column by. The value must be a number. |
| `max` | body | `number` | no | Maximum value for the column. If the current value is greater than this value, an error will be thrown. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
