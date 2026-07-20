# Appwrite: Create table

Creates a new table in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbcreate-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columns` | string | no | Array of column definitions to create. Each column should contain: key (string), type (string: string, integer, float, boolean, datetime, relationship), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `databaseId` | string | yes | Database ID. |
| `indexes` | string | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of column keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |
| `permissions` | string | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `tableId` | string | yes | Unique Id. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | string | yes | Table name. Max length: 128 chars. |
| `permissions[]` | array<string> | no | An array of permissions strings. By default, no user is granted with any permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `rowSecurity` | boolean | no | Enables configuring permissions for individual rows. A user needs one of row or table level permissions to access a row. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | boolean | no | Is table enabled? When set to 'disabled', users cannot access the table but Server SDKs with and API key can still read and write to the table. No data is lost when this is toggled. |
| `columns[]` | array<object> | no | Array of column definitions to create. Each column should contain: key (string), type (string: string, integer, float, boolean, datetime, relationship), size (integer, required for string type), required (boolean, optional), default (mixed, optional), array (boolean, optional), and type-specific options. |
| `indexes[]` | array<object> | no | Array of index definitions to create. Each index should contain: key (string), type (string: key, fulltext, unique, spatial), attributes (array of column keys), orders (array of ASC/DESC, optional), and lengths (array of integers, optional). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$createdAt": "string",
      "$id": "string",
      "$permissions": [
        "string"
      ],
      "$updatedAt": "string",
      "columns": [
        "string"
      ],
      "databaseId": "string",
      "enabled": true,
      "indexes": [
        {}
      ],
      "name": "Ava Chen",
      "rowSecurity": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$createdAt` | string | Table creation date in ISO 8601 format. |
| `$id` | string | Table ID. |
| `$permissions` | array<string> | Table permissions. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `$updatedAt` | string | Table update date in ISO 8601 format. |
| `columns` | array<string> | Table columns. |
| `databaseId` | string | Database ID. |
| `enabled` | boolean | Table enabled. Can be 'enabled' or 'disabled'. When disabled, the table is inaccessible to users, but remains accessible to Server SDKs using API keys. |
| `indexes` | array<object> | Table indexes. |
| `name` | string | Table name. |
| `rowSecurity` | boolean | Whether row-level permissions are enabled. [Learn more about permissions](https://appwrite.io/docs/permissions). |

## Native endpoint

Through the native Appwrite API, this operation is `POST /tablesdb/{databaseId}/tables` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbcreate-table.md) for the provider-specific parameters and requirements.

