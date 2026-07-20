# Shippify: Update Pickup Point

Updates pickup details for deliveries in Shippify.

```
PUT https://connect.mindcloud.co/v1/universal/shippify/latest/actions/update-pickup-point
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/update-pickup-point" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deliveryIds": "string",
  "deliveryChanges": {},
  "recalculatePrice": true,
  "reorderRoute": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippify/latest/actions/update-pickup-point', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deliveryIds": "string",
    "deliveryChanges": {},
    "recalculatePrice": true,
    "reorderRoute": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliveryIds` | string | yes | Comma-separated Shippify delivery identifiers to update, up to 10 per request. |
| `deliveryChanges` | object | yes | Required object describing pickup contact and or pickup location changes. |
| `recalculatePrice` | boolean | yes | Whether Shippify should recalculate the delivery price after the update. |
| `reorderRoute` | boolean | yes | Whether Shippify should reorder the route after the update when the delivery belongs to a route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {
        "jobs": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Shippify result code. |
| `data.jobs` | string | Additional job identifier when Shippify creates a background process. |
| `message` | string | Shippify result message. |

## Native endpoint

Through the native Shippify API, this operation is `PATCH /v1/deliveries/pickup` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pickup-point.md) for the provider-specific parameters and requirements.

