# Baserow: Move Row

Moves an existing row in a Baserow table.

```
PUT https://connect.mindcloud.co/v1/universal/baserow/latest/actions/move-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/move-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": 1,
  "rowId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baserow/latest/actions/move-row', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": 1,
    "rowId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | number | yes | The Baserow table containing the row. |
| `rowId` | number | yes | The row to move. |
| `beforeId` | number | no | Move the row before this row ID. Leave empty to move it to the end. |
| `sendWebhookEvents` | boolean | no | Whether Baserow should emit webhook events for the mutation. |
| `userFieldNames` | boolean | no | Use user-facing field names in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": 1,
      "name": "Ava Chen",
      "order": "string",
      "started": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `order` | string |  |
| `started` | date |  |

## Native endpoint

Through the native Baserow API, this operation is `PATCH /api/database/rows/table/:table_id/:row_id/move/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-row.md) for the provider-specific parameters and requirements.

