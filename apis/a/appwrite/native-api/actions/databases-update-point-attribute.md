# Update point attribute with Appwrite

Updates the point attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/point/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update point attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `default` | body | `string` | no | Default value for attribute when not provided, array of two numbers [longitude, latitude], representing a single coordinate. Cannot be set when attribute is required. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#createCollection). |
| `key` | path | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default[]` | body | `array<string>` | no | Default value for attribute when not provided, array of two numbers [longitude, latitude], representing a single coordinate. Cannot be set when attribute is required. |
| `newKey` | body | `string` | no | New attribute key. |
