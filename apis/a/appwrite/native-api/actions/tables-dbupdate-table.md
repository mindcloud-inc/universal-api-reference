# Update table with Appwrite

Updates the table in your Appwrite project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update table](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `permissions` | body | `string` | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `tableId` | path | `string` | yes | Table ID. |
| `name` | body | `string` | yes | Table name. Max length: 128 chars. |
| `permissions[]` | body | `array<string>` | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `rowSecurity` | body | `boolean` | no | Enables configuring permissions for individual rows. A user needs one of row or table-level permissions to access a row. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | body | `boolean` | no | Is table enabled? When set to 'disabled', users cannot access the table but Server SDKs with and API key can still read and write to the table. No data is lost when this is toggled. |
