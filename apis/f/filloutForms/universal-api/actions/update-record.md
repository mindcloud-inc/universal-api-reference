# Fillout Forms: Update Record

Updates an existing record in Fillout.

```
PUT https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "base_abc123",
  "tableId": "tbl_abc123",
  "recordId": "d4b3c2a3-c46b-46a1-a8ec-81b664bb41cb",
  "record": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "base_abc123",
    "tableId": "tbl_abc123",
    "recordId": "d4b3c2a3-c46b-46a1-a8ec-81b664bb41cb",
    "record": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The unique identifier of the database. Example: `base_abc123`. |
| `tableId` | string | yes | The unique identifier of the table. You can also use the table name instead of the ID. Example: `tbl_abc123`. |
| `recordId` | string | yes | The UUID of the record to update. Example: `d4b3c2a3-c46b-46a1-a8ec-81b664bb41cb`. |
| `record` | object | yes | Fields to update with their new values. Only include fields you want to change. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "data": {},
      "fields": {},
      "id": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Record creation timestamp. |
| `data` | object | Record values keyed by field IDs. |
| `fields` | object | Record values keyed by field names. |
| `id` | string | Record identifier. |
| `updatedAt` | string | Record update timestamp. |

## Native endpoint

Through the native Fillout Forms API, this operation is `PATCH https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records/:recordId` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

