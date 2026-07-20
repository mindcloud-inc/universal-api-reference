# Get document with Appwrite

Retrieves the document from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents/{documentId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Get document](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `documentId` | path | `string` | yes | Document ID. |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. Send multiple values as a array. |
| `transactionId` | query | `string` | no | Transaction ID to read uncommitted changes within the transaction. |
