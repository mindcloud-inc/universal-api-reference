# Create string attribute with Appwrite

Creates a new string attribute in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections/{collectionId}/attributes/string`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create string attribute](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `collectionId` | path | `string` | yes | Collection ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/server/databases#databasesCreateCollection). |
| `key` | body | `string` | yes | Attribute Key. |
| `size` | body | `number` | yes | Attribute size for text attributes, in number of characters. |
| `required` | body | `boolean` | yes | Is attribute required? |
| `default` | body | `string` | no | Default value for attribute when not provided. Cannot be set when attribute is required. |
| `array` | body | `boolean` | no | Is attribute an array? |
| `encrypt` | body | `boolean` | no | Toggle encryption for the attribute. Encryption enhances security by not storing any plain text values in the database. However, encrypted attributes cannot be queried. |
