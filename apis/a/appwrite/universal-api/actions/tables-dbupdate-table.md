# Appwrite: Update table

Updates the table in your Appwrite project.

```
PUT https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbupdate-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbupdate-table" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbupdate-table', {
  method: 'PUT',
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
| `databaseId` | string | yes | Database ID. |
| `permissions` | string | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `tableId` | string | yes | Table ID. |
| `name` | string | yes | Table name. Max length: 128 chars. |
| `permissions[]` | array<string> | no | An array of permission strings. By default, the current permissions are inherited. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `rowSecurity` | boolean | no | Enables configuring permissions for individual rows. A user needs one of row or table-level permissions to access a row. [Learn more about permissions](https://appwrite.io/docs/permissions). |
| `enabled` | boolean | no | Is table enabled? When set to 'disabled', users cannot access the table but Server SDKs with and API key can still read and write to the table. No data is lost when this is toggled. |

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

Through the native Appwrite API, this operation is `PUT /tablesdb/{databaseId}/tables/{tableId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbupdate-table.md) for the provider-specific parameters and requirements.

