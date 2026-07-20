# Upsert documents with Appwrite

Upserts documents in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Upsert documents](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `documents` | body | `string` | no | Array of document data as JSON objects. May contain partial documents. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `documents[]` | body | `array<object>` | yes | Array of document data as JSON objects. May contain partial documents. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
