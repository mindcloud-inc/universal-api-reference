# Update float attribute with Appwrite

Updates the float attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/float/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update float attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | path | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `min` | body | `number` | no | Minimum value. |
| `max` | body | `number` | no | Maximum value. |
| `default` | body | `number` | yes | Default value. Cannot be set when required. |
| `newKey` | body | `string` | no | New Attribute Key. |
