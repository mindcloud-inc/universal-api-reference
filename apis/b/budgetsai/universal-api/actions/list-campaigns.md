# Budgets.ai: List Campaigns



```
GET https://connect.mindcloud.co/v1/universal/budgetsai/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Budgets.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/budgetsai/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&state=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "all"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/budgetsai/latest/actions/list-campaigns?${params}`, {
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
| `state` | string | yes | Use running, paused, or all to choose which campaigns Budgets.ai returns. Default: `all`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Budgets.ai API returns.

## Native endpoint

Through the native Budgets.ai API, this operation is `POST /api-product/incoming-webhook/fetch-all-campaigns` (base URL `https://myapiconnect.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

