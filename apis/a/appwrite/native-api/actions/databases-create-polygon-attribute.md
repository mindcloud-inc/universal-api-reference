# Create polygon attribute with Appwrite

Creates a new polygon attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/polygon`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create polygon attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `default` | body | `string` | no | Default value for attribute when not provided, three-dimensional array where the outer array holds one or more linear rings, [[[longitude, latitude], …], …], the first ring is the exterior boundary, any additional rings are interior holes, and each ring must start and end with the same coordinate pair. Cannot be set when attribute is required. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new collection using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `key` | body | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default[]` | body | `array<string>` | no | Default value for attribute when not provided, three-dimensional array where the outer array holds one or more linear rings, [[[longitude, latitude], …], …], the first ring is the exterior boundary, any additional rings are interior holes, and each ring must start and end with the same coordinate pair. Cannot be set when attribute is required. |
