# Update integer attribute with Appwrite

Updates the integer attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/integer/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update integer attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | path | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `min` | body | `number` | no | Minimum value |
| `max` | body | `number` | no | Maximum value |
| `default` | body | `number` | yes | Default value. Cannot be set when attribute is required. |
| `newKey` | body | `string` | no | New Attribute Key. |
