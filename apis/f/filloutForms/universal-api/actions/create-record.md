# Fillout Forms: Create Record

Creates a record in Fillout.

```
POST https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "base_abc123",
  "tableId": "tbl_abc123",
  "record": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "base_abc123",
    "tableId": "tbl_abc123",
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
| `record` | object | yes | Record data with field names or field IDs as keys and their corresponding values. Example: `[object Object]`. |

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

Through the native Fillout Forms API, this operation is `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

