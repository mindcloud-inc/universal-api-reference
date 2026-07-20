# Billwerkplus: Delete Customer

Soft-deletes a customer from Billwerkplus.

```
DELETE https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/delete-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/delete-customer?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/delete-customer?${params}`, {
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
      "created": "string",
      "deleted": "string",
      "dunningAmount": 1,
      "dunningInvoices": 1,
      "expiredSubscriptions": 1,
      "failedAmount": 1,
      "failedInvoices": 1,
      "handle": "string",
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
| `created` | string |  |
| `deleted` | string |  |
| `dunningAmount` | number |  |
| `dunningInvoices` | number |  |
| `expiredSubscriptions` | number |  |
| `failedAmount` | number |  |
| `failedInvoices` | number |  |
| `handle` | string |  |
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

Through the native Billwerkplus API, this operation is `DELETE /customer/:handle` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer.md) for the provider-specific parameters and requirements.

