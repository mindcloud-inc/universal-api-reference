# List documents with Appwrite

Retrieves a list of documents from your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [List documents](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `queries[]` | query | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. Send multiple values as a array. |
| `transactionId` | query | `string` | no | Transaction ID to read uncommitted changes within the transaction. |
| `total` | query | `boolean` | no | When set to false, the total count returned will be 0 and will not be calculated. |
