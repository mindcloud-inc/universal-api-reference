# FraudLabs Pro: Feedback Payment

Updates payment feedback in FraudLabs Pro.

```
PUT https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "status": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/feedback-payment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "status": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The email address tied to the payment order. |
| `status` | string | yes | The final payment status. |
| `message` | string | yes | The message returned from the payment gateway. |
| `fraudlabspro_id` | string | no | The FraudLabs Pro transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | The result returned from the payment feedback API. |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `POST v2/payment/feedback` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/feedback-payment.md) for the provider-specific parameters and requirements.

