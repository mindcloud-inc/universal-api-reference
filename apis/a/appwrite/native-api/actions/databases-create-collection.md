# Create collections with Appwrite

Creates collections in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/collections`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create collections](https://appwrite.io/docs/references/cloud/server-rest/databases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributes` | body | `string` | no | Array of attribute definitions to create. Each attribute should contain: key (string), type (string: string, integer, float, boolean, datetime), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `databaseId` | path | `string` | yes | Database ID. |
| `indexes` | body | `string` | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of attribute keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |
| `permissions` | body | `string` | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `collectionId` | body | `string` | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Collection name. Max length: 128 chars. |
| `permissions[]` | body | `array<string>` | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `documentSecurity` | body | `boolean` | no | Enables configuring permissions for individual documents. A user needs one of document or collection level permissions to access a document. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | body | `boolean` | no | Is collection enabled? When set to 'disabled', users cannot access the collection but Server SDKs with and API key can still read and write to the collection. No data is lost when this is toggled. |
| `attributes[]` | body | `array<object>` | no | Array of attribute definitions to create. Each attribute should contain: key (string), type (string: string, integer, float, boolean, datetime), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `indexes[]` | body | `array<object>` | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of attribute keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |
