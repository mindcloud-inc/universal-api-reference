# Upsert a row with Appwrite

Upserts a row in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows/{rowId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Upsert a row](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `permissions` | body | `string` | no | An array of permissions strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `tableId` | path | `string` | yes | Table ID. |
| `rowId` | path | `string` | yes | Row ID. |
| `data` | body | `object` | no | Row data as JSON object. Include all required columns of the row to be created or updated. |
| `permissions[]` | body | `array<string>` | no | An array of permissions strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
