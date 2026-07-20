# Increment document attribute with Appwrite

Increments the document attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents/{documentId}/{attribute}/increment`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Increment document attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `documentId` | path | `string` | yes | Document ID. |
| `attribute` | path | `string` | yes | Attribute key. |
| `value` | body | `number` | no | Value to increment the attribute by. The value must be a number. |
| `max` | body | `number` | no | Maximum value for the attribute. If the current value is greater than this value, an error will be thrown. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
