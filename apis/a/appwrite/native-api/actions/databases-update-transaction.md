# Update transaction with Appwrite

Updates the transaction in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/transactions/{transactionId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update transaction](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionId` | path | `string` | yes | Transaction ID. |
| `commit` | body | `boolean` | no | Commit transaction? |
| `rollback` | body | `boolean` | no | Rollback transaction? |
