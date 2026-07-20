# ProfitWell: Create Or Update Customer Trait

Creates or updates a customer trait in ProfitWell.

```
PUT https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-or-update-customer-trait
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-or-update-customer-trait" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "trait": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/create-or-update-customer-trait', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "trait": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no | The customer ID to add or update a trait for. |
| `email` | string | no | The customer email to add or update a trait for. Applies to all customers with this email. |
| `category` | string | yes | The trait category. |
| `trait` | string | yes | The trait value. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `PUT /v2/customer_traits/trait/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-customer-trait.md) for the provider-specific parameters and requirements.

