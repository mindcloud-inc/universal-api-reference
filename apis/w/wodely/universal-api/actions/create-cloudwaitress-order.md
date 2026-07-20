# Wodely: Create CloudWaitress Order



```
POST https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-cloudwaitress-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-cloudwaitress-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wodely/latest/actions/create-cloudwaitress-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `secret` | string | no | CloudWaitress webhook secret value. |
| `event` | string | no | CloudWaitress webhook event identifier. |
| `eventId` | string | no | CloudWaitress webhook event ID. |
| `restaurantId` | string | no | CloudWaitress restaurant identifier. |
| `data` | object | no | CloudWaitress webhook data object containing the order payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {},
      "status": 1,
      "title": "string",
      "traceId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | object |  |
| `status` | number |  |
| `title` | string |  |
| `traceId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Wodely API, this operation is `POST /cloudwaitress/order` (base URL `https://api.wodely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-cloudwaitress-order.md) for the provider-specific parameters and requirements.

