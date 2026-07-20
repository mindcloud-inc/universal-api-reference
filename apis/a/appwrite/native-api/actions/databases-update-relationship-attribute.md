# Update relationship attribute with Appwrite

Updates the relationship attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/{key}/relationship`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update relationship attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | path | `string` | yes | Attribute Key. |
| `onDelete` | body | `string` | no | Constraints option |
| `newKey` | body | `string` | no | New Attribute Key. |
