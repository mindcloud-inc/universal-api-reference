# EODHD: Get Fundamental Highlights

Retrieves fundamental highlights for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-fundamental-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-fundamental-highlights?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-fundamental-highlights?${params}`, {
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
      "BookValue": 1,
      "DilutedEpsTTM": 1,
      "DividendShare": 1,
      "DividendYield": 1,
      "EarningsShare": 1,
      "EBITDA": 1,
      "GrossProfitTTM": 1,
      "MarketCapitalization": 1,
      "PEGRatio": 1,
      "PERatio": 1,
      "RevenueTTM": 1,
      "WallStreetTargetPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BookValue` | number | Book value. |
| `DilutedEpsTTM` | number | Trailing twelve-month diluted EPS. |
| `DividendShare` | number | Dividend per share. |
| `DividendYield` | number | Dividend yield. |
| `EarningsShare` | number | Earnings per share. |
| `EBITDA` | number | EBITDA. |
| `GrossProfitTTM` | number | Trailing twelve-month gross profit. |
| `MarketCapitalization` | number | Market capitalization. |
| `PEGRatio` | number | PEG ratio. |
| `PERatio` | number | Price-to-earnings ratio. |
| `RevenueTTM` | number | Trailing twelve-month revenue. |
| `WallStreetTargetPrice` | number | Wall Street target price. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fundamental-highlights.md) for the provider-specific parameters and requirements.

