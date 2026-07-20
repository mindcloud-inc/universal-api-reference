# Create boolean attribute with Appwrite

Creates a new boolean attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/boolean`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create boolean attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `key` | body | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `boolean` | no | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `array` | body | `boolean` | no | Is attribute an array? |
