# EODHD: Get Analyst Ratings

Retrieves analyst ratings for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-analyst-ratings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-analyst-ratings?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-analyst-ratings?${params}`, {
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
      "Buy": 1,
      "Hold": 1,
      "Rating": 1,
      "Sell": 1,
      "StrongBuy": 1,
      "StrongSell": 1,
      "TargetPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Buy` | number | Buy recommendation count. |
| `Hold` | number | Hold recommendation count. |
| `Rating` | number | Aggregate rating value. |
| `Sell` | number | Sell recommendation count. |
| `StrongBuy` | number | Strong-buy recommendation count. |
| `StrongSell` | number | Strong-sell recommendation count. |
| `TargetPrice` | number | Analyst target price. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analyst-ratings.md) for the provider-specific parameters and requirements.

