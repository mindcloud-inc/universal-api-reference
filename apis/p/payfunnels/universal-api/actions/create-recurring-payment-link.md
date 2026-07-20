# Payfunnels: Create Recurring Payment Link

Creates a recurring payment link in Payfunnels.

```
POST https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-recurring-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-recurring-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "description": "string",
  "amount": 1,
  "interval": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-recurring-payment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "description": "string",
    "amount": 1,
    "interval": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Payment link title. |
| `description` | string | yes | Detailed description of the payment link. |
| `currencyCode` | list | no | ISO 4217 currency code for the payment link, for example USD or GBP. |
| `amount` | number | yes | Recurring payment amount. |
| `interval` | string | yes | Recurring interval. Supported values are day, week, month, and year. |
| `trialDays` | number | no | Optional trial period in days. Must be greater than 2 days. |
| `isTaxable` | boolean | no | Whether the default tax rate should be applied. |
| `forwardProcessingFees` | boolean | no | Whether processing fees should be added to the payment link. |
| `coupon[]` | array<object> | no | Optional coupon definitions to apply at checkout as an array of objects. |
| `displayBillingAddress` | boolean | no | Prompt the customer for a billing address. |
| `displayShippingAddress` | boolean | no | Prompt the customer for a shipping address. |
| `enableTermOfService` | boolean | no | Require the customer to accept terms of service. |
| `additionalFields[]` | array<object> | no | Additional checkout fields as an array of objects. |
| `oneTimeSetupFeeProductId` | string | no | Optional one-time setup fee product ID to include in the payment link. |

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
      "oneTimeSetupFeeProductId": "string",
      "title": "string",
      "trialDays": 1,
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
| `oneTimeSetupFeeProductId` | string |  |
| `title` | string |  |
| `trialDays` | number |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Payfunnels API, this operation is `POST /v1/paymentlinks/recurring` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recurring-payment-link.md) for the provider-specific parameters and requirements.

