# Create enum attribute with Appwrite

Creates a new enum attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/enum`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create enum attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `elements` | body | `string` | no | Array of enum values. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | body | `string` | yes | Attribute Key. |
| `elements[]` | body | `array<string>` | yes | Array of enum values. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | no | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `array` | body | `boolean` | no | Is attribute an array? |
