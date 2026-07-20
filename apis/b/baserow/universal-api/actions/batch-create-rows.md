# Baserow: Batch Create Rows

Creates multiple rows in a Baserow table.

```
POST https://connect.mindcloud.co/v1/universal/baserow/latest/actions/batch-create-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Baserow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/batch-create-rows" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/baserow/latest/actions/batch-create-rows', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | number | yes | The Baserow table where rows will be created. |
| `userFieldNames` | boolean | no | Use user-facing field names in the request and response. |
| `before` | number | no | Create the new rows before the given row ID. |
| `includeMetadata` | boolean | no | Include update metadata in the response. |
| `sendWebhookEvents` | boolean | no | Whether Baserow should emit webhook events for the mutation. |
| `view` | number | no | Optional view context for permissions and default values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "active": true,
          "id": 1,
          "name": "Ava Chen",
          "order": "string",
          "started": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].active` | boolean |  |
| `items[].id` | number |  |
| `items[].name` | string |  |
| `items[].order` | string |  |
| `items[].started` | date |  |

## Native endpoint

Through the native Baserow API, this operation is `POST /api/database/rows/table/:table_id/batch/` (base URL `https://api.baserow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-create-rows.md) for the provider-specific parameters and requirements.

