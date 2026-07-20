# Commerce Layer: Delete Manual Tax Calculator



```
DELETE https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/delete-manual-tax-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Commerce Layer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/delete-manual-tax-calculator?connectionId=$CONNECTION_ID&id=AbCdEfGhIj" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "AbCdEfGhIj"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commerceLayer/latest/actions/delete-manual-tax-calculator?${params}`, {
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
| `id` | string | yes | The manual tax calculator ID to delete. Example: `AbCdEfGhIj`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Commerce Layer API returns.

## Native endpoint

Through the native Commerce Layer API, this operation is `DELETE /api/manual_tax_calculators/:id` (base URL `{{credentials.coreApiEndpoint}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-manual-tax-calculator.md) for the provider-specific parameters and requirements.

