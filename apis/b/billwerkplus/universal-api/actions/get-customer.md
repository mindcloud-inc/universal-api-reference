# Billwerkplus: Get Customer

Retrieves a customer from Billwerkplus.

```
GET https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-customer?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-customer?${params}`, {
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
| `handle` | string | yes | Customer handle. |

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

Through the native Billwerkplus API, this operation is `GET /customer/:handle` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

