# Financial Modeling Prep: Get Key Metrics

Retrieves key metrics from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-key-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-key-metrics?connectionId=$CONNECTION_ID&symbol=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-key-metrics?${params}`, {
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
| `symbol` | string | yes | Stock ticker symbol, such as AAPL. Example: `AAPL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "enterpriseValue": 1,
      "fiscalYear": "string",
      "freeCashFlowYield": 1,
      "marketCap": 1,
      "peRatio": 1,
      "period": "string",
      "returnOnEquity": 1,
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `enterpriseValue` | number |  |
| `fiscalYear` | string |  |
| `freeCashFlowYield` | number |  |
| `marketCap` | number |  |
| `peRatio` | number |  |
| `period` | string |  |
| `returnOnEquity` | number |  |
| `symbol` | string |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /key-metrics` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-key-metrics.md) for the provider-specific parameters and requirements.

