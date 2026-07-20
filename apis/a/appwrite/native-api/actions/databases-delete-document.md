# Delete document with Appwrite

Deletes the document from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents/{documentId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete document](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `documentId` | path | `string` | yes | Document ID. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
