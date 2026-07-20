# Finnhub: Get Stock Quote

Retrieves a stock quote from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-quote?connectionId=$CONNECTION_ID&symbol=e.g.%20AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "e.g. AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-stock-quote?${params}`, {
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
| `symbol` | string | yes | Company symbol for the quote, such as AAPL. Example: `e.g. AAPL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "c": 1,
      "d": 1,
      "dp": 1,
      "h": 1,
      "l": 1,
      "o": 1,
      "pc": 1,
      "t": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `c` | number | Current price. |
| `d` | number | Price change. |
| `dp` | number | Percent change. |
| `h` | number | High price of the day. |
| `l` | number | Low price of the day. |
| `o` | number | Open price of the day. |
| `pc` | number | Previous close price. |
| `t` | number | Unix timestamp. |

## Native endpoint

Through the native Finnhub API, this operation is `GET /quote` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock-quote.md) for the provider-specific parameters and requirements.

