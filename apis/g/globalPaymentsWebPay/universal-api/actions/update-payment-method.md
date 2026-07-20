# Global Payments WebPay: Update Payment Method

Updates a payment method in Global Payments WebPay.

```
PUT https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/update-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/update-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/update-payment-method', {
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
| `id` | string | yes | Global Payments payment method ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card": {
        "expiry_month": "string",
        "expiry_year": "string",
        "masked_number_last4": "string"
      },
      "fingerprint": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "usage_mode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card.expiry_month` | string |  |
| `card.expiry_year` | string |  |
| `card.masked_number_last4` | string |  |
| `fingerprint` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `usage_mode` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `PATCH /payment-methods/{id}` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-method.md) for the provider-specific parameters and requirements.

