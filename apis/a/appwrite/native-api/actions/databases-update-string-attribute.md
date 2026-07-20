# Update string attribute with Appwrite

Updates the string attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/string/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update string attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `key` | path | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | yes | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `size` | body | `number` | no | Maximum size of the string attribute. |
| `newKey` | body | `string` | no | New Attribute Key. |
