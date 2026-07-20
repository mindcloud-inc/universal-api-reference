# Delete index with Appwrite

Deletes the index from your Appwrite project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/indexes/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Delete index](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `key` | path | `string` | yes | Index Key. |
