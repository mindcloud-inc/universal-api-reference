# Create document with Appwrite

Creates a new document in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/documents`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create document](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `documents` | body | `string` | no | Array of documents data as JSON objects. |
| `permissions` | body | `string` | no | An array of permissions strings. By default, only the current user is granted all permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). Make sure to define attributes before creating documents. |
| `documentId` | body | `string` | no | Document ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `data` | body | `object` | no | Document data as JSON object. |
| `permissions[]` | body | `array<string>` | no | An array of permissions strings. By default, only the current user is granted all permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `documents[]` | body | `array<object>` | no | Array of documents data as JSON objects. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
