# Payfunnels: Create Pay What You Want Payment Link

Creates a pay-what-you-want payment link in Payfunnels.

```
POST https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-pay-what-you-want-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-pay-what-you-want-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-pay-what-you-want-payment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Pay-what-you-want payment link title. |
| `description` | string | yes | Detailed description of the payment link. |
| `currencyCode` | list | no | ISO 4217 currency code for the payment link, for example USD or GBP. |
| `allowOneTime` | boolean | no | Whether one-time payments are allowed. The provider default is true. |
| `allowRecurring` | boolean | no | Whether recurring payments are allowed. The provider default is false. |
| `isTaxable` | boolean | no | Whether the default tax rate should be applied. |
| `forwardProcessingFees` | boolean | no | Whether processing fees should be added to the payment link. |
| `displayBillingAddress` | boolean | no | Prompt the customer for a billing address. |
| `displayShippingAddress` | boolean | no | Prompt the customer for a shipping address. |
| `enableTermOfService` | boolean | no | Require the customer to accept terms of service. |
| `additionalFields[]` | array<object> | no | Additional checkout fields as an array of objects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalFields": [
        {}
      ],
      "allowOneTime": true,
      "allowRecurring": true,
      "currencyCode": "string",
      "description": "string",
      "displayBillingAddress": true,
      "displayShippingAddress": true,
      "enableTermOfService": true,
      "forwardProcessingFees": true,
      "id": "string",
      "isTaxable": true,
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
| `allowOneTime` | boolean |  |
| `allowRecurring` | boolean |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `displayBillingAddress` | boolean |  |
| `displayShippingAddress` | boolean |  |
| `enableTermOfService` | boolean |  |
| `forwardProcessingFees` | boolean |  |
| `id` | string |  |
| `isTaxable` | boolean |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Payfunnels API, this operation is `POST /v1/paymentlinks/paywhatyouwant` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pay-what-you-want-payment-link.md) for the provider-specific parameters and requirements.

