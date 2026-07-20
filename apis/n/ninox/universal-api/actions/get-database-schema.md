# Ninox: Get Database Schema

Retrieves a database schema from Ninox.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-database-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-database-schema?connectionId=$CONNECTION_ID&teamId=YcHTn3ir8XNSp5EXK&dbId=database_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-database-schema?${params}`, {
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
| `teamId` | string | yes | Workspace ID that owns the database. Example: `YcHTn3ir8XNSp5EXK`. |
| `dbId` | string | yes | Database ID to retrieve. Example: `database_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "modifiedAt": "string",
      "name": "Ava Chen",
      "tables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Database creation timestamp. |
| `id` | string | Database ID. |
| `modifiedAt` | string | Database last-modified timestamp. |
| `name` | string | Database name. |
| `tables` | array<object> | Tables in the database schema. |

## Native endpoint

Through the native Ninox API, this operation is `GET teams/:teamid/databases/:dbid` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-schema.md) for the provider-specific parameters and requirements.

