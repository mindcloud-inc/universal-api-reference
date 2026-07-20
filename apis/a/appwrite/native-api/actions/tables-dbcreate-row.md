# Create row with Appwrite

Creates a new row in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/tablesdb/{databaseId}/tables/{tableId}/rows`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create row](https://appwrite.io/docs/references/cloud/server-rest/tablesdb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database ID. |
| `permissions` | body | `string` | no | An array of permissions strings. By default, only the current user is granted all permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `rows` | body | `string` | no | Array of rows data as JSON objects. |
| `tableId` | path | `string` | yes | Table ID. You can create a new table using the Database service [server integration](https://appwrite.io/docs/references/cloud/server-dart/tablesDB#createTable). Make sure to define columns before creating rows. |
| `rowId` | body | `string` | no | Row ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `data` | body | `object` | no | Row data as JSON object. |
| `permissions[]` | body | `array<string>` | no | An array of permissions strings. By default, only the current user is granted all permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `rows[]` | body | `array<object>` | no | Array of rows data as JSON objects. |
| `transactionId` | body | `string` | no | Transaction ID for staging the operation. |
