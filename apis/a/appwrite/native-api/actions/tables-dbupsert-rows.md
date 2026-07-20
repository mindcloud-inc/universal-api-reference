# Upsert rows with Appwrite

Upserts rows in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Upsert rows](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `rows` | body | `string` | no | Array of row data as JSON objects. May contain partial rows. |
| `tableId` | path | `string` | yes | Table ID. |
| `rows[]` | body | `array<object>` | yes | Array of row data as JSON objects. May contain partial rows. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
