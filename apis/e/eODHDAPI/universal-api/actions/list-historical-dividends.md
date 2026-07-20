# EODHD: List Historical Dividends

Retrieves historical dividends for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-historical-dividends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-historical-dividends?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-historical-dividends?${params}`, {
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
| `from` | date | no | Start date in `YYYY-MM-DD` format. Example: `2000-01-01`. |
| `to` | date | no | End date in `YYYY-MM-DD` format. Example: `2025-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "period": "string",
      "recordDate": "2026-05-07T12:00:00.000Z",
      "unadjustedValue": 1,
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Dividend currency. |
| `date` | date | Dividend date. |
| `declarationDate` | date | Declaration date. |
| `paymentDate` | date | Payment date. |
| `period` | string | Dividend period. |
| `recordDate` | date | Record date. |
| `unadjustedValue` | number | Unadjusted dividend value. |
| `value` | number | Dividend value. |

## Native endpoint

Through the native EODHD API, this operation is `GET /div/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-historical-dividends.md) for the provider-specific parameters and requirements.

