# EODHD: Get Full Fundamentals

Retrieves full fundamentals for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-full-fundamentals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-full-fundamentals?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-full-fundamentals?${params}`, {
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
| `symbol` | string | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. Example: `AAPL.US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AnalystRatings": {},
      "Earnings": {},
      "ESGScores": {},
      "Financials": {},
      "General": {},
      "Highlights": {},
      "Holders": {},
      "InsiderTransactions": {},
      "SharesStats": {},
      "SplitsDividends": {},
      "Technicals": {},
      "Valuation": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AnalystRatings` | object | Analyst rating summary. |
| `Earnings` | object | Earnings data. |
| `ESGScores` | object | ESG score data. |
| `Financials` | object | Financial statement data. |
| `General` | object | General company metadata. |
| `Highlights` | object | Key financial highlights. |
| `Holders` | object | Holder data. |
| `InsiderTransactions` | object | Insider transaction data. |
| `SharesStats` | object | Share statistics. |
| `SplitsDividends` | object | Splits and dividends summary. |
| `Technicals` | object | Technical summary. |
| `Valuation` | object | Valuation metrics. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-fundamentals.md) for the provider-specific parameters and requirements.

