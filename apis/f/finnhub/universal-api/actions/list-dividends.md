# Finnhub: List Dividends

Retrieves dividends from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-dividends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-dividends?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL&from=2025-01-01&to=2025-12-31" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL",
  "from": "2025-01-01",
  "to": "2025-12-31"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-dividends?${params}`, {
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
| `symbol` | string | yes | Company symbol, such as AAPL. Example: `e.g. AAPL`. |
| `from` | string | yes | Start date in YYYY-MM-DD format. Example: `2025-01-01`. |
| `to` | string | yes | End date in YYYY-MM-DD format. Example: `2025-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adjustedAmount": 1,
      "amount": 1,
      "currency": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "frequency": "string",
      "payDate": "2026-05-07T12:00:00.000Z",
      "recordDate": "2026-05-07T12:00:00.000Z",
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjustedAmount` | number |  |
| `amount` | number |  |
| `currency` | string |  |
| `date` | date |  |
| `declarationDate` | date |  |
| `frequency` | string |  |
| `payDate` | date |  |
| `recordDate` | date |  |
| `symbol` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/dividend` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dividends.md) for the provider-specific parameters and requirements.

