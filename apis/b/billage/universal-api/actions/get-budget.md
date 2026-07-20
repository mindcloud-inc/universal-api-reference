# Billage: Get Budget

Retrieves a budget record from Billage.

```
GET https://connect.mindcloud.co/v1/universal/billage/latest/actions/get-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billage/latest/actions/get-budget?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billage/latest/actions/get-budget?${params}`, {
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
| `id` | number | yes | Billage budget ID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billage API returns.

## Native endpoint

Through the native Billage API, this operation is `GET /v2/budgets/:id` (base URL `https://app.getbillage.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-budget.md) for the provider-specific parameters and requirements.

