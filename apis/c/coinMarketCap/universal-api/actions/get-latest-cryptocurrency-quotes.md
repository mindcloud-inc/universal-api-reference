# CoinMarketCap: Get Latest Cryptocurrency Quotes

Retrieves latest cryptocurrency quotes from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-cryptocurrency-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-cryptocurrency-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-cryptocurrency-quotes?${params}`, {
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
| `id` | string | no | CoinMarketCap cryptocurrency ID, for example 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "circulating_supply": 1,
      "cmc_rank": 1,
      "date_added": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "infinite_supply": true,
      "is_active": 1,
      "is_fiat": 1,
      "last_updated": "2026-05-07T12:00:00.000Z",
      "max_supply": 1,
      "minted_market_cap": 1,
      "name": "Ava Chen",
      "num_market_pairs": 1,
      "quote": [
        {
          "cex_volume_24h": 1,
          "dex_volume_24h": 1,
          "fully_diluted_market_cap": 1,
          "id": 1,
          "last_updated": "2026-05-07T12:00:00.000Z",
          "market_cap": 1,
          "market_cap_dominance": 1,
          "minted_market_cap": 1,
          "percent_change_1h": 1,
          "percent_change_24h": 1,
          "percent_change_30d": 1,
          "percent_change_60d": 1,
          "percent_change_7d": 1,
          "percent_change_90d": 1,
          "price": 1,
          "symbol": "string",
          "volume_24h": 1,
          "volume_change_24h": 1
        }
      ],
      "slug": "string",
      "symbol": "string",
      "tags": [
        {
          "category": "string",
          "name": "Ava Chen",
          "slug": "string"
        }
      ],
      "total_supply": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `circulating_supply` | number |  |
| `cmc_rank` | number |  |
| `date_added` | date |  |
| `id` | number |  |
| `infinite_supply` | boolean |  |
| `is_active` | number |  |
| `is_fiat` | number |  |
| `last_updated` | date |  |
| `max_supply` | number |  |
| `minted_market_cap` | number |  |
| `name` | string |  |
| `num_market_pairs` | number |  |
| `quote[].cex_volume_24h` | number |  |
| `quote[].dex_volume_24h` | number |  |
| `quote[].fully_diluted_market_cap` | number |  |
| `quote[].id` | number |  |
| `quote[].last_updated` | date |  |
| `quote[].market_cap` | number |  |
| `quote[].market_cap_dominance` | number |  |
| `quote[].minted_market_cap` | number |  |
| `quote[].percent_change_1h` | number |  |
| `quote[].percent_change_24h` | number |  |
| `quote[].percent_change_30d` | number |  |
| `quote[].percent_change_60d` | number |  |
| `quote[].percent_change_7d` | number |  |
| `quote[].percent_change_90d` | number |  |
| `quote[].price` | number |  |
| `quote[].symbol` | string |  |
| `quote[].volume_24h` | number |  |
| `quote[].volume_change_24h` | number |  |
| `slug` | string |  |
| `symbol` | string |  |
| `tags[].category` | string |  |
| `tags[].name` | string |  |
| `tags[].slug` | string |  |
| `total_supply` | number |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v3/cryptocurrency/quotes/latest` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-cryptocurrency-quotes.md) for the provider-specific parameters and requirements.

