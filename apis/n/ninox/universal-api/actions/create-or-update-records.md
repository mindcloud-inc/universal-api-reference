# Ninox: Create Or Update Records

Creates or updates multiple records in a Ninox table.

```
POST https://connect.mindcloud.co/v1/universal/ninox/latest/actions/create-or-update-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/create-or-update-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id",
  "tableId": "table_id",
  "records": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninox/latest/actions/create-or-update-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "YcHTn3ir8XNSp5EXK",
    "dbId": "database_id",
    "tableId": "table_id",
    "records": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Workspace ID that owns the database. Example: `YcHTn3ir8XNSp5EXK`. |
| `dbId` | string | yes | Database ID that owns the table. Example: `database_id`. |
| `tableId` | string | yes | Table ID to create or update records in. Example: `table_id`. |
| `records` | list<object> | yes | Array of record payloads to create or update. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_cd": "string",
      "_cu": "string",
      "_id": 1,
      "_md": "string",
      "_mu": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_cd` | string | Record creation timestamp. |
| `_cu` | string | Record creator. |
| `_id` | number | Record ID. |
| `_md` | string | Record last-modified timestamp. |
| `_mu` | string | Record last modifier. |

## Native endpoint

Through the native Ninox API, this operation is `POST teams/:teamid/databases/:dbid/tables/:tableid/records` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-records.md) for the provider-specific parameters and requirements.

