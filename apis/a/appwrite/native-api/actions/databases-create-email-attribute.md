# Create email attribute with Appwrite

Creates a new email attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/email`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create email attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | body | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | no | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `array` | body | `boolean` | no | Is attribute an array? |
