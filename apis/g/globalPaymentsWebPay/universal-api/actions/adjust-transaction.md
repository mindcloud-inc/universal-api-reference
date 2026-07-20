# Global Payments WebPay: Adjust Transaction

Updates a transaction by adjusting it in Global Payments WebPay.

```
PUT https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/adjust-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/adjust-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/adjust-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Global Payments transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": {
        "id": "string"
      },
      "amount": "string",
      "country": "string",
      "currency": "string",
      "id": "string",
      "reference": "string",
      "status": "string",
      "time_created": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action.id` | string |  |
| `amount` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `id` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `time_created` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /transactions/{id}/adjustment` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/adjust-transaction.md) for the provider-specific parameters and requirements.

