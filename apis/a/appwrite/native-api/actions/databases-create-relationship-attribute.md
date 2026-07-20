# Create relationship attribute with Appwrite

Creates a new relationship attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/relationship`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create relationship attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `relatedCollectionId` | body | `string` | yes | Related Collection ID. |
| `type` | body | `string` | yes | Relation type |
| `twoWay` | body | `boolean` | no | Is Two Way? |
| `key` | body | `string` | no | Attribute Key. |
| `twoWayKey` | body | `string` | no | Two Way Attribute Key. |
| `onDelete` | body | `string` | no | Constraints option |
