# Create index with Appwrite

Creates a new index in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/indexes`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create index](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributes` | body | `string` | no | Array of attributes to index. Maximum of 100 attributes are allowed, each 32 characters long. |
| `databaseId` | path | `string` | yes | Database ID. |
| `lengths` | body | `string` | no | Length of index. Maximum of 100 |
| `orders` | body | `string` | no | Array of index orders. Maximum of 100 orders are allowed. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `key` | body | `string` | yes | Index Key. |
| `type` | body | `string` | yes | Index type. |
| `attributes[]` | body | `array<string>` | yes | Array of attributes to index. Maximum of 100 attributes are allowed, each 32 characters long. |
| `orders[]` | body | `array<string>` | no | Array of index orders. Maximum of 100 orders are allowed. |
| `lengths[]` | body | `array<number>` | no | Length of index. Maximum of 100 |
