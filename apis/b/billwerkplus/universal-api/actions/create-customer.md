# Billwerkplus: Create Customer

Creates a customer in Billwerkplus.

```
POST https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `handle` | string | yes | Per-account unique customer handle. |
| `email` | string | no | Customer email address. |
| `firstName` | string | no | Customer first name. |
| `lastName` | string | no | Customer last name. |
| `country` | string | no | Customer country as ISO 3166-1 alpha-2. |
| `test` | boolean | no | Create the customer in test mode. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeSubscriptions": 1,
      "cancelledAmount": 1,
      "cancelledInvoices": 1,
      "cancelledSubscriptions": 1,
      "country": "string",
      "created": "string",
      "dunningAmount": 1,
      "dunningInvoices": 1,
      "email": "ava@example.com",
      "expiredSubscriptions": 1,
      "failedAmount": 1,
      "failedInvoices": 1,
      "firstName": "Ava",
      "handle": "string",
      "lastName": "Chen",
      "nonRenewingSubscriptions": 1,
      "onHoldSubscriptions": 1,
      "pendingAdditionalCostAmount": 1,
      "pendingAdditionalCosts": 1,
      "pendingAmount": 1,
      "pendingCreditAmount": 1,
      "pendingCredits": 1,
      "pendingInvoices": 1,
      "refundedAmount": 1,
      "settledAmount": 1,
      "settledInvoices": 1,
      "subscriptions": 1,
      "test": true,
      "transferredAdditionalCostAmount": 1,
      "transferredAdditionalCosts": 1,
      "transferredCreditAmount": 1,
      "transferredCredits": 1,
      "trialActiveSubscriptions": 1,
      "trialCancelledSubscriptions": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeSubscriptions` | number |  |
| `cancelledAmount` | number |  |
| `cancelledInvoices` | number |  |
| `cancelledSubscriptions` | number |  |
| `country` | string |  |
| `created` | string |  |
| `dunningAmount` | number |  |
| `dunningInvoices` | number |  |
| `email` | string |  |
| `expiredSubscriptions` | number |  |
| `failedAmount` | number |  |
| `failedInvoices` | number |  |
| `firstName` | string |  |
| `handle` | string |  |
| `lastName` | string |  |
| `nonRenewingSubscriptions` | number |  |
| `onHoldSubscriptions` | number |  |
| `pendingAdditionalCostAmount` | number |  |
| `pendingAdditionalCosts` | number |  |
| `pendingAmount` | number |  |
| `pendingCreditAmount` | number |  |
| `pendingCredits` | number |  |
| `pendingInvoices` | number |  |
| `refundedAmount` | number |  |
| `settledAmount` | number |  |
| `settledInvoices` | number |  |
| `subscriptions` | number |  |
| `test` | boolean |  |
| `transferredAdditionalCostAmount` | number |  |
| `transferredAdditionalCosts` | number |  |
| `transferredCreditAmount` | number |  |
| `transferredCredits` | number |  |
| `trialActiveSubscriptions` | number |  |
| `trialCancelledSubscriptions` | number |  |

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /customer` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

