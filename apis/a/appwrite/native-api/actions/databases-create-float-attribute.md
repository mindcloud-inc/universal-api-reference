# Create float attribute with Appwrite

Creates a new float attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/float`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create float attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | body | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `min` | body | `number` | no | Minimum value. |
| `max` | body | `number` | no | Maximum value. |
| `default` | body | `number` | no | Default value. Cannot be set when required. |
| `array` | body | `boolean` | no | Is attribute an array? |
