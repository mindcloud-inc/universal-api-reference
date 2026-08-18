# Stripe: Retrieve Payment Method – Southern Botanical



```
GET https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-payment-method-southern-botanical
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-payment-method-southern-botanical?connectionId=$CONNECTION_ID&paymentMethodId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentMethodId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripe/latest/actions/retrieve-payment-method-southern-botanical?${params}`, {
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
| `paymentMethodId` | string | yes | Stripe PaymentMethod ID to retrieve (for example, pm_...). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingDetails": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "card": {
        "brand": "string",
        "country": "string",
        "funding": "string",
        "last4": "string",
        "networks": {
          "available": [
            "string"
          ]
        },
        "wallet": {
          "type": "string"
        }
      },
      "created": 1,
      "customer": "string",
      "id": "string",
      "livemode": true,
      "object": "string",
      "type": "string",
      "usBankAccount": {
        "accountType": "string",
        "bankName": "Ava Chen",
        "last4": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingDetails.email` | string |  |
| `billingDetails.name` | string |  |
| `card.brand` | string |  |
| `card.country` | string |  |
| `card.funding` | string |  |
| `card.last4` | string |  |
| `card.networks.available[]` | string |  |
| `card.wallet.type` | string |  |
| `created` | number |  |
| `customer` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `object` | string |  |
| `type` | string |  |
| `usBankAccount.accountType` | string |  |
| `usBankAccount.bankName` | string |  |
| `usBankAccount.last4` | string |  |

## Native endpoint

Through the native Stripe API, this operation is `GET payment_methods/:paymentMethodId` (base URL `https://api.stripe.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-payment-method-southern-botanical.md) for the provider-specific parameters and requirements.

