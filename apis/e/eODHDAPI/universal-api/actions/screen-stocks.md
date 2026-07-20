# EODHD: Screen Stocks

Finds stocks in EODHD API using screener filters.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/screen-stocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/screen-stocks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/screen-stocks?${params}`, {
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
| `filters` | string | no | JSON filter expression array for the screener endpoint. Example: `market_capitalization,>,1000000000,exchange,=,us`. |
| `signals` | string | no | Comma-separated predefined screener signals. Example: `wallstreet_lo,bookvalue_neg`. |
| `sort` | string | no | Sort field and direction, for example market_capitalization.desc. Example: `market_capitalization.desc`. |
| `limit` | number | no | Maximum number of screener results to return. Example: `10`. |
| `offset` | number | no | Number of screener results to skip. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "dividendYield": 1,
      "earningsShare": 1,
      "exchange": "string",
      "industry": "string",
      "lastDayClosePrice": 1,
      "marketCapitalization": 1,
      "name": "Ava Chen",
      "sector": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Ticker code. |
| `dividendYield` | number | Dividend yield. |
| `earningsShare` | number | Earnings per share. |
| `exchange` | string | Exchange code. |
| `industry` | string | Industry. |
| `lastDayClosePrice` | number | Last-day close price. |
| `marketCapitalization` | number | Market capitalization. |
| `name` | string | Company name. |
| `sector` | string | Sector. |

## Native endpoint

Through the native EODHD API, this operation is `GET /screener` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/screen-stocks.md) for the provider-specific parameters and requirements.

