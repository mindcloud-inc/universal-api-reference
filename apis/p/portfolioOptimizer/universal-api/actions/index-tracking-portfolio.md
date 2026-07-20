# Portfolio Optimizer: Index Tracking Portfolio



```
GET https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/index-tracking-portfolio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Portfolio Optimizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/index-tracking-portfolio?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/index-tracking-portfolio?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `G[]` | array<array> | no | Optional matrix defining asset groups. |
| `l[]` | array<number> | no | Optional minimum weights for each asset. |
| `u[]` | array<number> | no | Optional maximum weights for each asset. |
| `uG[]` | array<number> | no | Optional maximum weights for the defined asset groups. |
| `wMax` | number | no | Optional upper bound on total portfolio exposure. |
| `wMin` | number | no | Optional lower bound on total portfolio exposure. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Portfolio Optimizer API returns.

## Native endpoint

Through the native Portfolio Optimizer API, this operation is `POST /v1/portfolios/replication/index-tracking` (base URL `https://api.portfoliooptimizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/index-tracking-portfolio.md) for the provider-specific parameters and requirements.

