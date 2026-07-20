# Stripe: Search Payment Intents

Finds payment intents in Stripe by search query.

```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-payment-intents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-payment-intents?connectionId=$CONNECTION_ID&limit=25&offset=0&query=status%3A'requires_payment_method'" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "status:'requires_payment_method'"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/search-payment-intents?${params}`, {
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
| `query` | string | yes | The query argument that is going to be passed onto the Stripe Api Example: `status:'requires_payment_method'`. |
| `limit` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | string | no |  |
| `expand[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "amountCapturable": 1,
      "amountDetails": {
        "shipping": {
          "amount": 1,
          "fromPostalCode": "string",
          "toPostalCode": "string"
        }
      },
      "amountReceived": 1,
      "application": {},
      "applicationFeeAmount": {},
      "automaticPaymentMethods": {
        "allowRedirects": "string",
        "enabled": true
      },
      "canceledAt": {},
      "cancellationReason": {},
      "captureMethod": "string",
      "clientSecret": "string",
      "confirmationMethod": "string",
      "created": 1,
      "currency": "string",
      "customer": "string",
      "description": "string",
      "excludedPaymentMethodTypes": {},
      "id": "string",
      "lastPaymentError": {},
      "latestCharge": "string",
      "livemode": true,
      "metadata": {
        "guest": "string",
        "module": "string",
        "orderNumber": "string"
      },
      "nextAction": {},
      "object": "string",
      "onBehalfOf": {},
      "paymentDetails": {
        "customerReference": {},
        "orderReference": "string"
      },
      "paymentMethod": "string",
      "paymentMethodConfigurationDetails": {
        "id": "string",
        "parent": {}
      },
      "paymentMethodOptions": {
        "amazonPay": {
          "expressCheckoutElementSessionId": {}
        },
        "card": {
          "installments": {},
          "mandateOptions": {},
          "network": {},
          "requestThreeDSecure": "string",
          "setupFutureUsage": "string"
        },
        "link": {
          "persistentToken": {},
          "setupFutureUsage": "https://example.com"
        }
      },
      "paymentMethodTypes": [
        "string"
      ],
      "processing": {},
      "receiptEmail": {},
      "review": {},
      "setupFutureUsage": {},
      "shipping": {
        "address": {
          "city": "string",
          "country": "string",
          "line1": "string",
          "line2": {},
          "postalCode": "string",
          "state": "string"
        },
        "carrier": {},
        "name": "Ava Chen",
        "phone": "string",
        "trackingNumber": {}
      },
      "source": {},
      "statementDescriptor": {},
      "statementDescriptorSuffix": {},
      "status": "string",
      "transferData": {},
      "transferGroup": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `amountCapturable` | number |  |
| `amountDetails.shipping.amount` | number |  |
| `amountDetails.shipping.fromPostalCode` | string |  |
| `amountDetails.shipping.toPostalCode` | string |  |
| `amountReceived` | number |  |
| `application` | object |  |
| `applicationFeeAmount` | object |  |
| `automaticPaymentMethods.allowRedirects` | string |  |
| `automaticPaymentMethods.enabled` | boolean |  |
| `canceledAt` | object |  |
| `cancellationReason` | object |  |
| `captureMethod` | string |  |
| `clientSecret` | string |  |
| `confirmationMethod` | string |  |
| `created` | number |  |
| `currency` | string |  |
| `customer` | string |  |
| `description` | string |  |
| `excludedPaymentMethodTypes` | object |  |
| `id` | string |  |
| `lastPaymentError` | object |  |
| `latestCharge` | string |  |
| `livemode` | boolean |  |
| `metadata.guest` | string |  |
| `metadata.module` | string |  |
| `metadata.orderNumber` | string |  |
| `nextAction` | object |  |
| `object` | string |  |
| `onBehalfOf` | object |  |
| `paymentDetails.customerReference` | object |  |
| `paymentDetails.orderReference` | string |  |
| `paymentMethod` | string |  |
| `paymentMethodConfigurationDetails.id` | string |  |
| `paymentMethodConfigurationDetails.parent` | object |  |
| `paymentMethodOptions.amazonPay.expressCheckoutElementSessionId` | object |  |
| `paymentMethodOptions.card.installments` | object |  |
| `paymentMethodOptions.card.mandateOptions` | object |  |
| `paymentMethodOptions.card.network` | object |  |
| `paymentMethodOptions.card.requestThreeDSecure` | string |  |
| `paymentMethodOptions.card.setupFutureUsage` | string |  |
| `paymentMethodOptions.link.persistentToken` | object |  |
| `paymentMethodOptions.link.setupFutureUsage` | string |  |
| `paymentMethodTypes[]` | string |  |
| `processing` | object |  |
| `receiptEmail` | object |  |
| `review` | object |  |
| `setupFutureUsage` | object |  |
| `shipping.address.city` | string |  |
| `shipping.address.country` | string |  |
| `shipping.address.line1` | string |  |
| `shipping.address.line2` | object |  |
| `shipping.address.postalCode` | string |  |
| `shipping.address.state` | string |  |
| `shipping.carrier` | object |  |
| `shipping.name` | string |  |
| `shipping.phone` | string |  |
| `shipping.trackingNumber` | object |  |
| `source` | object |  |
| `statementDescriptor` | object |  |
| `statementDescriptorSuffix` | object |  |
| `status` | string |  |
| `transferData` | object |  |
| `transferGroup` | object |  |

## Native endpoint

Through the native Stripe API, this operation is `GET payment_intents/search` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-payment-intents.md) for the provider-specific parameters and requirements.

