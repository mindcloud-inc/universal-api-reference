# CoinMarketCap: Convert Price

Converts amounts between currencies using CoinMarketCap pricing.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/convert-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/convert-price?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/convert-price?${params}`, {
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
| `amount` | string | no | Amount to convert. |
| `convert` | string | no | Target conversion currency symbol, for example USD. |
| `symbol` | string | no | Source cryptocurrency symbol, for example BTC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "id": 1,
      "last_updated": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "quote": {
        "USD": {
          "last_updated": "2026-05-07T12:00:00.000Z",
          "price": 1
        }
      },
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `id` | number |  |
| `last_updated` | date |  |
| `name` | string |  |
| `quote.USD.last_updated` | date |  |
| `quote.USD.price` | number |  |
| `symbol` | string |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v2/tools/price-conversion` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-price.md) for the provider-specific parameters and requirements.

