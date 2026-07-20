# ProfitWell: Remove Trait Category

Deletes a trait category from ProfitWell.

```
DELETE https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/remove-trait-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProfitWell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/remove-trait-category?connectionId=$CONNECTION_ID&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profitWell/latest/actions/remove-trait-category?${params}`, {
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
| `category` | string | yes | The category to remove from every customer that has it. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ProfitWell API returns.

## Native endpoint

Through the native ProfitWell API, this operation is `DELETE /v2/customer_traits/category/` (base URL `https://api.profitwell.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-trait-category.md) for the provider-specific parameters and requirements.

