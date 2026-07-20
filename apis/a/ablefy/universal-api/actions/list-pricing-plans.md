# Ablefy: List Pricing Plans

Retrieves pricing plans from Ablefy.

```
GET https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/list-pricing-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ablefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/list-pricing-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ablefy/latest/actions/list-pricing-plans?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ablefy API returns.

## Native endpoint

Through the native Ablefy API, this operation is `GET /api/pricing_plans` (base URL `https://api.myablefy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pricing-plans.md) for the provider-specific parameters and requirements.

