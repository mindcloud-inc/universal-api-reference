# ProfitWell: Remove Customer Trait

Deletes a customer trait from ProfitWell.

```
DELETE https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/remove-customer-trait
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/remove-customer-trait?connectionId=$CONNECTION_ID&category=string&trait=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string",
  "trait": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/remove-customer-trait?${params}`, {
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
| `customerId` | string | no | The customer ID to remove a trait from. |
| `email` | string | no | The customer email to remove a trait from. Applies to all customers with this email. |
| `category` | string | yes | The trait category. |
| `trait` | string | yes | The trait value to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `DELETE /v2/customer_traits/trait/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-customer-trait.md) for the provider-specific parameters and requirements.

