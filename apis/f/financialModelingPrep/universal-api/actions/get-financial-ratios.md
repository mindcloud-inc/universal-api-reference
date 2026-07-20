# Financial Modeling Prep: Get Financial Ratios

Retrieves financial ratios from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-financial-ratios
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-financial-ratios?connectionId=$CONNECTION_ID&symbol=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-financial-ratios?${params}`, {
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
      "currentRatio": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "fiscalYear": "string",
      "grossProfitMargin": 1,
      "netProfitMargin": 1,
      "operatingProfitMargin": 1,
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
| `currentRatio` | number |  |
| `date` | date |  |
| `fiscalYear` | string |  |
| `grossProfitMargin` | number |  |
| `netProfitMargin` | number |  |
| `operatingProfitMargin` | number |  |
| `period` | string |  |
| `returnOnEquity` | number |  |
| `symbol` | string |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /ratios` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-financial-ratios.md) for the provider-specific parameters and requirements.

