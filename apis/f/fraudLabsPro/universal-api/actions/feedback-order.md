# FraudLabs Pro: Feedback Order

Updates order feedback in FraudLabs Pro.

```
PUT https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "action": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "action": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The FraudLabs Pro transaction ID or merchant order ID. |
| `action` | string | yes | Feedback action to send. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fraudlabspro_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fraudlabspro_id` | string | The FraudLabs Pro ID that was updated. |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `POST v2/order/feedback` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/feedback-order.md) for the provider-specific parameters and requirements.

