# Financial Modeling Prep: Get Dividends

Retrieves dividends from Financial Modeling Prep.

```
GET https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-dividends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Financial Modeling Prep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-dividends?connectionId=$CONNECTION_ID&symbol=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/get-dividends?${params}`, {
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
      "adjDividend": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "dividend": 1,
      "frequency": "string",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "recordDate": "2026-05-07T12:00:00.000Z",
      "symbol": "string",
      "yield": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjDividend` | number |  |
| `date` | date |  |
| `declarationDate` | date |  |
| `dividend` | number |  |
| `frequency` | string |  |
| `paymentDate` | date |  |
| `recordDate` | date |  |
| `symbol` | string |  |
| `yield` | number |  |

## Native endpoint

Through the native Financial Modeling Prep API, this operation is `GET /dividends` (base URL `https://financialmodelingprep.com/stable`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dividends.md) for the provider-specific parameters and requirements.

