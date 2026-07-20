# Queue: Pause Service Checkout

Pauses a service checkout subscription in Queue.

```
PUT https://connect.mindcloud.co/v1/universal/queue/latest/actions/pause-service-checkout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/queue/latest/actions/pause-service-checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serviceCheckoutId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/queue/latest/actions/pause-service-checkout', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serviceCheckoutId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `serviceCheckoutId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Queue API, this operation is `POST service_checkouts/:service_checkout_id/pause` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-service-checkout.md) for the provider-specific parameters and requirements.

