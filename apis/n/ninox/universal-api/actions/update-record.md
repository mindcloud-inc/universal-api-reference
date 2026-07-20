# Ninox: Update Record

Updates a record in a Ninox table.

```
PUT https://connect.mindcloud.co/v1/universal/ninox/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninox/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "YcHTn3ir8XNSp5EXK",
  "dbId": "database_id",
  "tableId": "table_id",
  "recordId": "record_id",
  "fields": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninox/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "YcHTn3ir8XNSp5EXK",
    "dbId": "database_id",
    "tableId": "table_id",
    "recordId": "record_id",
    "fields": "[object Object]"
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
| `tableId` | string | yes | Table ID that owns the record. Example: `table_id`. |
| `recordId` | string | yes | Record ID to update. Example: `record_id`. |
| `fields` | object | yes | Object of field values to update. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "fields": {},
      "id": 1,
      "modifiedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Record creation timestamp. |
| `fields` | object | Record field values. |
| `id` | number | Record ID. |
| `modifiedAt` | number | Record last-modified timestamp. |

## Native endpoint

Through the native Ninox API, this operation is `PUT teams/:teamid/databases/:dbid/tables/:tableid/records/:recordid` (base URL `https://api.ninox.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

