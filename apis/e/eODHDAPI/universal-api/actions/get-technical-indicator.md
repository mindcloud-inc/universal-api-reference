# EODHD: Get Technical Indicator

Retrieves a technical indicator for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-technical-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-technical-indicator?connectionId=$CONNECTION_ID&symbol=AAPL.US&function=sma" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US",
  "function": "sma"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-technical-indicator?${params}`, {
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
| `function` | string | yes | Technical indicator function, for example sma. Example: `sma`. |
| `period` | number | no | Indicator calculation period. Example: `50`. |
| `from` | date | no | Start date in YYYY-MM-DD format. Example: `2025-01-01`. |
| `to` | date | no | End date in YYYY-MM-DD format. Example: `2025-12-31`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | string | no | Result order, for example d for descending. Example: `d`. |
| `splitadjustedOnly` | boolean | no | Return split-adjusted values only when supported. |
| `filter` | string | no | Optional response filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Indicator date. |
| `value` | number | Technical indicator value. |

## Native endpoint

Through the native EODHD API, this operation is `GET /technical/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-technical-indicator.md) for the provider-specific parameters and requirements.

