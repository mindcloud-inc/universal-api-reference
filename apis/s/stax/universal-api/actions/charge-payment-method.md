# Stax: Charge Payment Method

Charges a payment method in Stax.

```
POST https://connect.mindcloud.co/v1/universal/stax/latest/actions/charge-payment-method
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stax/latest/actions/charge-payment-method" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stax/latest/actions/charge-payment-method', {
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
| `meta` | object | no | Charge metadata |
| `paymentMethodId` | string | no | Payment method identifier |
| `preAuth` | boolean | no | Pre-authorization flag |
| `total` | number | no | Charge total in dollars |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "currency": "string",
      "customerId": "string",
      "id": "string",
      "isRefundable": true,
      "isVoidable": true,
      "paymentMethodId": "string",
      "success": true,
      "total": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `currency` | string | Transaction currency. |
| `customerId` | string | Associated customer identifier. |
| `id` | string | Stax transaction identifier. |
| `isRefundable` | boolean | Whether the transaction can be refunded. |
| `isVoidable` | boolean | Whether the transaction can be voided. |
| `paymentMethodId` | string | Associated payment method identifier. |
| `success` | boolean | Whether the transaction succeeded. |
| `total` | number | Transaction total amount. |
| `type` | string | Transaction type. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Stax API, this operation is `POST /charge` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/charge-payment-method.md) for the provider-specific parameters and requirements.

