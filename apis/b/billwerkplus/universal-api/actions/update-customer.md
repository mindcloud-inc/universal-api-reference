# Billwerkplus: Update Customer

Updates a customer in Billwerkplus.

```
PUT https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/update-customer', {
  method: 'PUT',
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
| `handle` | string | yes | Customer handle. |
| `email` | string | no | Updated customer email address. |
| `firstName` | string | no | Updated customer first name. |
| `lastName` | string | no | Updated customer last name. |
| `company` | string | no | Updated customer company name. |

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
      "company": "string",
      "created": "string",
      "dunningAmount": 1,
      "dunningInvoices": 1,
      "expiredSubscriptions": 1,
      "failedAmount": 1,
      "failedInvoices": 1,
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
| `company` | string |  |
| `created` | string |  |
| `dunningAmount` | number |  |
| `dunningInvoices` | number |  |
| `expiredSubscriptions` | number |  |
| `failedAmount` | number |  |
| `failedInvoices` | number |  |
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

Through the native Billwerkplus API, this operation is `PUT /customer/:handle` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

