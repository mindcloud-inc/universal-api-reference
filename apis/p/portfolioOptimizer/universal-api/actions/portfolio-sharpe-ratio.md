# Portfolio Optimizer: Portfolio Sharpe Ratio



```
GET https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/portfolio-sharpe-ratio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Portfolio Optimizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/portfolio-sharpe-ratio?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/portfolio-sharpe-ratio?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "portfolios": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `portfolios` | array<object> | Portfolios with computed Sharpe ratios. |

## Native endpoint

Through the native Portfolio Optimizer API, this operation is `POST /v1/portfolios/analysis/mean-variance/sharpe-ratio` (base URL `https://api.portfoliooptimizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/portfolio-sharpe-ratio.md) for the provider-specific parameters and requirements.

