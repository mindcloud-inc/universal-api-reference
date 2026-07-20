# Shippify: Update Delivery

Updates delivery details in Shippify by ID or reference.

```
PUT https://connect.mindcloud.co/v1/universal/shippify/latest/actions/update-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/update-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deliveryIds[]": [
    "string"
  ],
  "deliveryChanges": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippify/latest/actions/update-delivery', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deliveryIds[]": ["string"],
    "deliveryChanges": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliveryIds[]` | array<string> | yes | Required array of up to 10 Shippify delivery identifiers to update. |
| `referenceIds[]` | array<string> | no | Optional array of delivery reference identifiers to update instead of delivery IDs. |
| `deliveryChanges` | object | yes | Required object describing the delivery fields to update, such as dropoff, packages, tags, cod, or referenceId. |
| `recalculatePrice` | boolean | no | Whether Shippify should recalculate the delivery price after the update. |
| `reorderRoute` | boolean | no | Whether Shippify should reorder the route after the update when the delivery belongs to a route. |
| `recalculateCity` | boolean | no | Whether Shippify should recalculate the city after the update. |

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
      "deliveriesCreated": [
        [
          {}
        ]
      ],
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
| `deliveriesCreated[]` | array<object> | Additional deliveries created by the update workflow when applicable. |
| `message` | string | Shippify result message. |

## Native endpoint

Through the native Shippify API, this operation is `PATCH /v1/deliveries/dropoff` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-delivery.md) for the provider-specific parameters and requirements.

