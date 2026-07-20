# Payfunnels: Get Payment

Retrieves a payment from Payfunnels by ID.

```
GET https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-payment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-payment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the payment to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {},
      "cardLast4": "string",
      "coupon": {},
      "createdAt": "string",
      "currencyCode": "string",
      "customer": {},
      "description": "string",
      "id": "string",
      "metadata": {},
      "processingFeeAmount": 1,
      "products": [
        {}
      ],
      "quantity": 1,
      "refundAmount": 1,
      "setupFeeAmount": 1,
      "shippingAddress": {},
      "status": "string",
      "taxAmount": 1,
      "title": "string",
      "totalAmountPaid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `cardLast4` | string |  |
| `coupon` | object |  |
| `createdAt` | string |  |
| `currencyCode` | string |  |
| `customer` | object |  |
| `description` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `processingFeeAmount` | number |  |
| `products` | array<object> |  |
| `quantity` | number |  |
| `refundAmount` | number |  |
| `setupFeeAmount` | number |  |
| `shippingAddress` | object |  |
| `status` | string |  |
| `taxAmount` | number |  |
| `title` | string |  |
| `totalAmountPaid` | number |  |

## Native endpoint

Through the native Payfunnels API, this operation is `GET /v1/payments/{id}` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment.md) for the provider-specific parameters and requirements.

