# EODHD: Get Cash Flow Fundamentals

Retrieves cash flow fundamentals for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-cash-flow-fundamentals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-cash-flow-fundamentals?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-cash-flow-fundamentals?${params}`, {
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
      "capitalExpenditures": 1,
      "changeInCash": 1,
      "currency_symbol": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "filing_date": "2026-05-07T12:00:00.000Z",
      "freeCashFlow": 1,
      "totalCashFromOperatingActivities": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capitalExpenditures` | number | Capital expenditures. |
| `changeInCash` | number | Change in cash. |
| `currency_symbol` | string | Statement currency. |
| `date` | date | Statement date. |
| `filing_date` | date | Filing date. |
| `freeCashFlow` | number | Free cash flow when returned. |
| `totalCashFromOperatingActivities` | number | Operating cash flow. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cash-flow-fundamentals.md) for the provider-specific parameters and requirements.

