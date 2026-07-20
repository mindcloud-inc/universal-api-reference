# Update documents with Appwrite

Updates the documents in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update documents](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `queries` | body | `string` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `data` | body | `object` | no | Document data as JSON object. Include only attribute and value pairs to be updated. |
| `queries[]` | body | `array<string>` | no | Array of query strings generated using the Query class provided by the SDK. [Learn more about queries](https://appwrite.io/docs/queries). Maximum of 100 queries are allowed, each 4096 characters long. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
