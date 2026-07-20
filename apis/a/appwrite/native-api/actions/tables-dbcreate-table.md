# Create table with Appwrite

Creates a new table in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create table](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns` | body | `string` | no | Array of column definitions to create. Each column should contain: key (string), type (string: string, integer, float, boolean, datetime, relationship), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `databaseId` | path | `string` | yes | Database ID. |
| `indexes` | body | `string` | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of column keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |
| `permissions` | body | `string` | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `tableId` | body | `string` | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Table name. Max length: 128 chars. |
| `permissions[]` | body | `array<string>` | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `rowSecurity` | body | `boolean` | no | Enables configuring permissions for individual rows. A user needs one of row or table level permissions to access a row. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | body | `boolean` | no | Is table enabled? When set to 'disabled', users cannot access the table but Server SDKs with and API key can still read and write to the table. No data is lost when this is toggled. |
| `columns[]` | body | `array<object>` | no | Array of column definitions to create. Each column should contain: key (string), type (string: string, integer, float, boolean, datetime, relationship), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `indexes[]` | body | `array<object>` | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of column keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |
