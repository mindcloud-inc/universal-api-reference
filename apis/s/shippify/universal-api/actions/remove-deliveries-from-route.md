# Shippify: Remove Deliveries From Route

Removes deliveries from an existing route in Shippify.

```
PUT https://connect.mindcloud.co/v1/universal/shippify/latest/actions/remove-deliveries-from-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/remove-deliveries-from-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "routeId": "string",
  "deliveries[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippify/latest/actions/remove-deliveries-from-route', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "routeId": "string",
    "deliveries[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `routeId` | string | yes | Identifier of the route that the deliveries should be removed from. |
| `deliveries[]` | array<string> | yes | Required array of delivery identifiers to remove from the route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {
        "jobs": [
          [
            {}
          ]
        ]
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
| `data.jobs[]` | array<object> | Background jobs created while updating the route. |
| `message` | string | Shippify result message. |

## Native endpoint

Through the native Shippify API, this operation is `PATCH /v1/routes/remove` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-deliveries-from-route.md) for the provider-specific parameters and requirements.

