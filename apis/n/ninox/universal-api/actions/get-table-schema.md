# Ninox: Get Table Schema

Retrieves a table schema from Ninox.

```
GET https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-table-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-table-schema?connectionId=$CONNECTION_ID&teamId=YcHTn3ir8XNSp5EXK&dbId=database_id&tableId=table_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id",
  "tableId": "table_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ninox/latest/actions/get-table-schema?${params}`, {
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
| `dbId` | string | yes | Database ID that owns the table. Example: `database_id`. |
| `tableId` | string | yes | Table ID to retrieve. Example: `table_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "sequence": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | Table field definitions. |
| `id` | string | Table ID. |
| `name` | string | Table name. |
| `sequence` | number | Table sequence number. |

## Native endpoint

Through the native Ninox API, this operation is `GET teams/:teamid/databases/:dbid/tables/:tableid` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-schema.md) for the provider-specific parameters and requirements.

