# Portfolio Optimizer: Empirical Covariance Matrix



```
GET https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/empirical-covariance-matrix
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Portfolio Optimizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/empirical-covariance-matrix?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portfolioOptimizer/latest/actions/empirical-covariance-matrix?${params}`, {
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
      "assetsCovarianceMatrix": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetsCovarianceMatrix` | array<array> | Estimated empirical covariance matrix. |

## Native endpoint

Through the native Portfolio Optimizer API, this operation is `POST /v1/assets/covariance/matrix/estimation/empirical` (base URL `https://api.portfoliooptimizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/empirical-covariance-matrix.md) for the provider-specific parameters and requirements.

