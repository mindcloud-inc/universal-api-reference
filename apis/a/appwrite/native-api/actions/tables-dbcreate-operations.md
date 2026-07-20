# Create operations with Appwrite

Creates operations in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/transactions/{transactionId}/operations`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create operations](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operations` | body | `string` | no | Array of staged operations. |
| `transactionId` | path | `string` | yes | Transaction ID. |
| `operations[]` | body | `array<object>` | no | Array of staged operations. |
