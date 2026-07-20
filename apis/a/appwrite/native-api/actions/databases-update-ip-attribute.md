# Update IP address attribute with Appwrite

Updates the IP address attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/ip/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update IP address attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | path | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | yes | Default value. Cannot be set when attribute is required. |
| `newKey` | body | `string` | no | New Attribute Key. |
