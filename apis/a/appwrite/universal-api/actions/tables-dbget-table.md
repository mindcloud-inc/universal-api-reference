# Appwrite: Get table

Retrieves the table from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-table?connectionId=$CONNECTION_ID&databaseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/tables-dbget-table?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | Database ID. |
| `tableId` | string | yes | Table ID. |

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

Through the native Appwrite API, this operation is `GET /tablesdb/{databaseId}/tables/{tableId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tables-dbget-table.md) for the provider-specific parameters and requirements.

