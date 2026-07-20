# Update document with Appwrite

Updates the document in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents/{documentId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update document](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `permissions` | body | `string` | no | An array of permissions strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `collectionId` | path | `string` | yes | Collection ID. |
| `documentId` | path | `string` | yes | Document ID. |
| `data` | body | `object` | no | Document data as JSON object. Include only attribute and value pairs to be updated. |
| `permissions[]` | body | `array<string>` | no | An array of permissions strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
