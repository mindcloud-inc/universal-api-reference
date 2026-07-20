# Billwerkplus: Cancel Subscription

Cancels a subscription in Billwerkplus.

```
DELETE https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-subscription?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/cancel-subscription?${params}`, {
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
| `handle` | string | yes | Subscription handle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activated": "string",
      "cancelledAmount": 1,
      "cancelledDate": "string",
      "cancelledInvoices": 1,
      "created": "string",
      "currency": "string",
      "customer": "string",
      "dunningAmount": 1,
      "dunningInvoices": 1,
      "expires": "string",
      "failedAmount": 1,
      "failedInvoices": 1,
      "firstPeriodStart": "string",
      "graceDuration": 1,
      "handle": "string",
      "hasStarted": true,
      "hostedPageLinks": {
        "paymentInfo": "https://example.com"
      },
      "inTrial": true,
      "isCancelled": true,
      "nextPeriodStart": "string",
      "paymentMethodAdded": true,
      "pendingAdditionalCostAmount": 1,
      "pendingAdditionalCosts": 1,
      "pendingAmount": 1,
      "pendingCreditAmount": 1,
      "pendingCredits": 1,
      "pendingInvoices": 1,
      "plan": "string",
      "planVersion": 1,
      "quantity": 1,
      "refundedAmount": 1,
      "renewalCount": 1,
      "renewing": true,
      "settledAmount": 1,
      "settledInvoices": 1,
      "startDate": "string",
      "state": "string",
      "test": true,
      "timezone": "string",
      "transferredAdditionalCostAmount": 1,
      "transferredAdditionalCosts": 1,
      "transferredCreditAmount": 1,
      "transferredCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated` | string |  |
| `cancelledAmount` | number |  |
| `cancelledDate` | string |  |
| `cancelledInvoices` | number |  |
| `created` | string |  |
| `currency` | string |  |
| `customer` | string |  |
| `dunningAmount` | number |  |
| `dunningInvoices` | number |  |
| `expires` | string |  |
| `failedAmount` | number |  |
| `failedInvoices` | number |  |
| `firstPeriodStart` | string |  |
| `graceDuration` | number |  |
| `handle` | string |  |
| `hasStarted` | boolean |  |
| `hostedPageLinks.paymentInfo` | string |  |
| `inTrial` | boolean |  |
| `isCancelled` | boolean |  |
| `nextPeriodStart` | string |  |
| `paymentMethodAdded` | boolean |  |
| `pendingAdditionalCostAmount` | number |  |
| `pendingAdditionalCosts` | number |  |
| `pendingAmount` | number |  |
| `pendingCreditAmount` | number |  |
| `pendingCredits` | number |  |
| `pendingInvoices` | number |  |
| `plan` | string |  |
| `planVersion` | number |  |
| `quantity` | number |  |
| `refundedAmount` | number |  |
| `renewalCount` | number |  |
| `renewing` | boolean |  |
| `settledAmount` | number |  |
| `settledInvoices` | number |  |
| `startDate` | string |  |
| `state` | string |  |
| `test` | boolean |  |
| `timezone` | string |  |
| `transferredAdditionalCostAmount` | number |  |
| `transferredAdditionalCosts` | number |  |
| `transferredCreditAmount` | number |  |
| `transferredCredits` | number |  |

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /subscription/:handle/cancel` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-subscription.md) for the provider-specific parameters and requirements.

