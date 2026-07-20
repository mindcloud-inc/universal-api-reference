# Portfolio Optimizer: Maximum Sharpe Ratio



```
GET https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/maximum-sharpe-ratio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Portfolio Optimizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/maximum-sharpe-ratio?connectionId=$CONNECTION_ID&mu%5B%5D=1&r_f=1&Sigma%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mu[]": "1",
  "r_f": "1",
  "Sigma[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/maximum-sharpe-ratio?${params}`, {
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
| `mu[]` | array<number> | yes | Required asset arithmetic returns vector. |
| `r_f` | number | yes | Required risk-free rate. |
| `Sigma[]` | array<array> | yes | Required asset covariance matrix. |

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

```json
{
  "success": true,
  "data": [
    {
      "assetsWeights": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetsWeights` | array<number> | Optimal asset weights for the maximum Sharpe ratio portfolio. |

## Native endpoint

Through the native Portfolio Optimizer API, this operation is `POST /v1/portfolio/optimization/maximum-sharpe-ratio` (base URL `https://api.portfoliooptimizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/maximum-sharpe-ratio.md) for the provider-specific parameters and requirements.

