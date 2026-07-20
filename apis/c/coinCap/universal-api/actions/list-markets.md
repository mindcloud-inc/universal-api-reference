# CoinCap: List Markets

Retrieves markets from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-markets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-markets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-markets?${params}`, {
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
| `exchangeId` | string | no | Filter by exchange id. Example: `binance`. |
| `baseSymbol` | string | no | Filter by base asset symbol. Example: `BTC`. |
| `baseId` | string | no | Filter by base asset id. Example: `bitcoin`. |
| `quoteSymbol` | string | no | Filter by quote asset symbol. Example: `USDT`. |
| `quoteId` | string | no | Filter by quote asset id. Example: `tether`. |
| `assetSymbol` | string | no | Filter by asset symbol on either side of the market. Example: `BTC`. |
| `assetId` | string | no | Filter by asset id on either side of the market. Example: `bitcoin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseId": "string",
      "baseSymbol": "string",
      "exchangeId": "string",
      "percentExchangeVolume": "string",
      "priceQuote": "string",
      "priceUsd": "string",
      "quoteId": "string",
      "quoteSymbol": "string",
      "rank": "string",
      "tradesCount24Hr": 1,
      "updated": 1,
      "volumeUsd24Hr": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseId` | string |  |
| `baseSymbol` | string |  |
| `exchangeId` | string |  |
| `percentExchangeVolume` | string |  |
| `priceQuote` | string |  |
| `priceUsd` | string |  |
| `quoteId` | string |  |
| `quoteSymbol` | string |  |
| `rank` | string |  |
| `tradesCount24Hr` | number |  |
| `updated` | number |  |
| `volumeUsd24Hr` | string |  |

## Native endpoint

Through the native CoinCap API, this operation is `GET /markets` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-markets.md) for the provider-specific parameters and requirements.

