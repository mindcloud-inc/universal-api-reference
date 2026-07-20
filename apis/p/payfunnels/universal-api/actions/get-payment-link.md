# Payfunnels: Get Payment Link

Retrieves a payment link from Payfunnels by ID.

```
GET https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-payment-link?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/get-payment-link?${params}`, {
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
| `id` | string | yes | The ID of the payment link to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalFields": [
        {}
      ],
      "amount": 1,
      "coupon": [
        {}
      ],
      "currencyCode": "string",
      "description": "string",
      "displayBillingAddress": true,
      "displayShippingAddress": true,
      "enableTermOfService": true,
      "forwardProcessingFees": true,
      "id": "string",
      "interval": "string",
      "isTaxable": true,
      "numberOfPayments": 1,
      "oneTimeSetupFeeProductId": "string",
      "paymentSchedule": {},
      "products": [
        {}
      ],
      "title": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalFields` | array<object> |  |
| `amount` | number |  |
| `coupon` | array<object> |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `displayBillingAddress` | boolean |  |
| `displayShippingAddress` | boolean |  |
| `enableTermOfService` | boolean |  |
| `forwardProcessingFees` | boolean |  |
| `id` | string |  |
| `interval` | string |  |
| `isTaxable` | boolean |  |
| `numberOfPayments` | number |  |
| `oneTimeSetupFeeProductId` | string |  |
| `paymentSchedule` | object |  |
| `products` | array<object> |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Payfunnels API, this operation is `GET /v1/paymentlinks/{id}` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-link.md) for the provider-specific parameters and requirements.

