# Financial Modeling Prep: Get Financial Scores

Retrieves financial scores from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-financial-scores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-financial-scores?connectionId=$CONNECTION_ID&symbol=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-financial-scores?${params}`, {
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
      "altmanZScore": 1,
      "marketCap": 1,
      "piotroskiScore": 1,
      "reportedCurrency": "string",
      "symbol": "string",
      "totalAssets": 1,
      "workingCapital": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altmanZScore` | number |  |
| `marketCap` | number |  |
| `piotroskiScore` | number |  |
| `reportedCurrency` | string |  |
| `symbol` | string |  |
| `totalAssets` | number |  |
| `workingCapital` | number |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /financial-scores` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-financial-scores.md) for the provider-specific parameters and requirements.

