# Update boolean attribute with Appwrite

Updates the boolean attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/boolean/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update boolean attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#createCollection). |
| `key` | path | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `boolean` | yes | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `newKey` | body | `string` | no | New attribute key. |
