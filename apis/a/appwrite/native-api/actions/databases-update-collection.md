# Update collection with Appwrite

Updates the collection in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/databases/{databaseId}/collections/{collectionId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update collection](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `permissions` | body | `string` | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `collectionId` | path | `string` | yes | Collection ID. |
| `name` | body | `string` | yes | Collection name. Max length: 128 chars. |
| `permissions[]` | body | `array<string>` | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `documentSecurity` | body | `boolean` | no | Enables configuring permissions for individual documents. A user needs one of document or collection level permissions to access a document. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | body | `boolean` | no | Is collection enabled? When set to 'disabled', users cannot access the collection but Server SDKs with and API key can still read and write to the collection. No data is lost when this is toggled. |
