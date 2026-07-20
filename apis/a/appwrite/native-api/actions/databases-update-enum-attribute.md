# Update enum attribute with Appwrite

Updates the enum attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/enum/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update enum attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `elements` | body | `string` | no | Updated list of enum values. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | path | `string` | yes | Attribute Key. |
| `elements[]` | body | `array<string>` | yes | Updated list of enum values. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | yes | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `newKey` | body | `string` | no | New Attribute Key. |
