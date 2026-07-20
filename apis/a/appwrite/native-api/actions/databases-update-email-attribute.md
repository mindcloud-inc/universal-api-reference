# Update email attribute with Appwrite

Updates the email attribute in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/email/{key}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update email attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. |
| `key` | path | `string` | yes | Attribute Key. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | yes | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `newKey` | body | `string` | no | New Attribute Key. |
