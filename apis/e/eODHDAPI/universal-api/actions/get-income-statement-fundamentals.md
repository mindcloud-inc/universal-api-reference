# EODHD: Get Income Statement Fundamentals

Retrieves income statement fundamentals for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-income-statement-fundamentals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-income-statement-fundamentals?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-income-statement-fundamentals?${params}`, {
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
      "currency_symbol": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "eps": 1,
      "filing_date": "2026-05-07T12:00:00.000Z",
      "grossProfit": 1,
      "netIncome": 1,
      "operatingIncome": 1,
      "totalRevenue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency_symbol` | string | Statement currency. |
| `date` | date | Statement date. |
| `eps` | number | Earnings per share. |
| `filing_date` | date | Filing date. |
| `grossProfit` | number | Gross profit. |
| `netIncome` | number | Net income. |
| `operatingIncome` | number | Operating income. |
| `totalRevenue` | number | Total revenue. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-income-statement-fundamentals.md) for the provider-specific parameters and requirements.

