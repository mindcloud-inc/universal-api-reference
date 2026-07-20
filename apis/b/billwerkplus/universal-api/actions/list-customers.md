# Billwerkplus: List Customers

Retrieves customers from Billwerkplus.

```
GET https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/list-customers?${params}`, {
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
| `handle` | string | no | Filter by exact customer handle. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Filter by customer email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
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
      "count": 1,
      "from": "string",
      "range": "string",
      "size": 1,
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[].activeSubscriptions` | number |  |
| `content[].cancelledAmount` | number |  |
| `content[].cancelledInvoices` | number |  |
| `content[].cancelledSubscriptions` | number |  |
| `content[].country` | string |  |
| `content[].created` | string |  |
| `content[].dunningAmount` | number |  |
| `content[].dunningInvoices` | number |  |
| `content[].email` | string |  |
| `content[].expiredSubscriptions` | number |  |
| `content[].failedAmount` | number |  |
| `content[].failedInvoices` | number |  |
| `content[].firstName` | string |  |
| `content[].handle` | string |  |
| `content[].lastName` | string |  |
| `content[].nonRenewingSubscriptions` | number |  |
| `content[].onHoldSubscriptions` | number |  |
| `content[].pendingAdditionalCostAmount` | number |  |
| `content[].pendingAdditionalCosts` | number |  |
| `content[].pendingAmount` | number |  |
| `content[].pendingCreditAmount` | number |  |
| `content[].pendingCredits` | number |  |
| `content[].pendingInvoices` | number |  |
| `content[].refundedAmount` | number |  |
| `content[].settledAmount` | number |  |
| `content[].settledInvoices` | number |  |
| `content[].subscriptions` | number |  |
| `content[].test` | boolean |  |
| `content[].transferredAdditionalCostAmount` | number |  |
| `content[].transferredAdditionalCosts` | number |  |
| `content[].transferredCreditAmount` | number |  |
| `content[].transferredCredits` | number |  |
| `content[].trialActiveSubscriptions` | number |  |
| `content[].trialCancelledSubscriptions` | number |  |
| `count` | number |  |
| `from` | string |  |
| `range` | string |  |
| `size` | number |  |
| `to` | string |  |

## Native endpoint

Through the native Billwerkplus API, this operation is `GET /list/customer` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

