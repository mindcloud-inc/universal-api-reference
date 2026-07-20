# Global Payments WebPay: Confirm Transaction

Updates a transaction by confirming it in Global Payments WebPay.

```
PUT https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/confirm-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Payments WebPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/confirm-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPaymentsWebPay/latest/actions/confirm-transaction', {
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
      "payment_method": {
        "apm": {
          "provider": "string",
          "provider_payer_name": "Ava Chen",
          "provider_payer_reference": "string",
          "provider_time_created": "string",
          "provider_transaction_reference": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payment_method.apm.provider` | string |  |
| `payment_method.apm.provider_payer_name` | string |  |
| `payment_method.apm.provider_payer_reference` | string |  |
| `payment_method.apm.provider_time_created` | string |  |
| `payment_method.apm.provider_transaction_reference` | string |  |

## Native endpoint

Through the native Global Payments WebPay API, this operation is `POST /transactions/{id}/confirmation` (base URL `https://apis.globalpay.com/ucp`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-transaction.md) for the provider-specific parameters and requirements.

