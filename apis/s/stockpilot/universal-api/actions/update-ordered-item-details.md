# Stockpilot: Update Ordered Item Details

Updates an ordered item in Stockpilot.

```
PUT https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/update-ordered-item-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/update-ordered-item-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "item_id": 1,
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/update-ordered-item-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "item_id": 1,
    "quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `item_id` | number | yes |  |
| `quantity` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Stockpilot API, this operation is `PATCH /orders/ordered-items/:item_id/update` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-ordered-item-details.md) for the provider-specific parameters and requirements.

