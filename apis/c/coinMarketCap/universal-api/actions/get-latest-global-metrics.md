# CoinMarketCap: Get Latest Global Metrics

Retrieves latest global crypto market metrics from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-global-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-global-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-global-metrics?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active_cryptocurrencies": 1,
      "active_exchanges": 1,
      "active_market_pairs": 1,
      "btc_dominance": 1,
      "btc_dominance_24h_percentage_change": 1,
      "btc_dominance_yesterday": 1,
      "defi_24h_percentage_change": 1,
      "defi_market_cap": 1,
      "defi_volume_24h": 1,
      "defi_volume_24h_reported": 1,
      "derivatives_24h_percentage_change": 1,
      "derivatives_volume_24h": 1,
      "derivatives_volume_24h_reported": 1,
      "eth_dominance": 1,
      "eth_dominance_24h_percentage_change": 1,
      "eth_dominance_yesterday": 1,
      "last_updated": "2026-05-07T12:00:00.000Z",
      "past_24h_incremental_crypto_number": 1,
      "past_30d_incremental_crypto_number": 1,
      "past_7d_incremental_crypto_number": 1,
      "quote": {
        "USD": {
          "altcoin_market_cap": 1,
          "altcoin_volume_24h": 1,
          "altcoin_volume_24h_reported": 1,
          "defi_24h_percentage_change": 1,
          "defi_market_cap": 1,
          "defi_volume_24h": 1,
          "defi_volume_24h_reported": 1,
          "derivatives_24h_percentage_change": 1,
          "derivatives_volume_24h": 1,
          "derivatives_volume_24h_reported": 1,
          "last_updated": "2026-05-07T12:00:00.000Z",
          "stablecoin_24h_percentage_change": 1,
          "stablecoin_market_cap": 1,
          "stablecoin_volume_24h": 1,
          "stablecoin_volume_24h_reported": 1,
          "total_market_cap": 1,
          "total_market_cap_yesterday": 1,
          "total_market_cap_yesterday_percentage_change": 1,
          "total_volume_24h": 1,
          "total_volume_24h_reported": 1,
          "total_volume_24h_yesterday": 1,
          "total_volume_24h_yesterday_percentage_change": 1
        }
      },
      "stablecoin_24h_percentage_change": 1,
      "stablecoin_market_cap": 1,
      "stablecoin_volume_24h": 1,
      "stablecoin_volume_24h_reported": 1,
      "today_change_percent": 1,
      "today_incremental_crypto_number": 1,
      "total_crypto_dex_currencies": 1,
      "total_cryptocurrencies": 1,
      "total_exchanges": 1,
      "tracked_yearly_number": {
        "maxIncrementalDate": "2026-05-07T12:00:00.000Z",
        "maxIncrementalNumber": 1,
        "minIncrementalDate": "2026-05-07T12:00:00.000Z",
        "minIncrementalNumber": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_cryptocurrencies` | number |  |
| `active_exchanges` | number |  |
| `active_market_pairs` | number |  |
| `btc_dominance` | number |  |
| `btc_dominance_24h_percentage_change` | number |  |
| `btc_dominance_yesterday` | number |  |
| `defi_24h_percentage_change` | number |  |
| `defi_market_cap` | number |  |
| `defi_volume_24h` | number |  |
| `defi_volume_24h_reported` | number |  |
| `derivatives_24h_percentage_change` | number |  |
| `derivatives_volume_24h` | number |  |
| `derivatives_volume_24h_reported` | number |  |
| `eth_dominance` | number |  |
| `eth_dominance_24h_percentage_change` | number |  |
| `eth_dominance_yesterday` | number |  |
| `last_updated` | date |  |
| `past_24h_incremental_crypto_number` | number |  |
| `past_30d_incremental_crypto_number` | number |  |
| `past_7d_incremental_crypto_number` | number |  |
| `quote.USD.altcoin_market_cap` | number |  |
| `quote.USD.altcoin_volume_24h` | number |  |
| `quote.USD.altcoin_volume_24h_reported` | number |  |
| `quote.USD.defi_24h_percentage_change` | number |  |
| `quote.USD.defi_market_cap` | number |  |
| `quote.USD.defi_volume_24h` | number |  |
| `quote.USD.defi_volume_24h_reported` | number |  |
| `quote.USD.derivatives_24h_percentage_change` | number |  |
| `quote.USD.derivatives_volume_24h` | number |  |
| `quote.USD.derivatives_volume_24h_reported` | number |  |
| `quote.USD.last_updated` | date |  |
| `quote.USD.stablecoin_24h_percentage_change` | number |  |
| `quote.USD.stablecoin_market_cap` | number |  |
| `quote.USD.stablecoin_volume_24h` | number |  |
| `quote.USD.stablecoin_volume_24h_reported` | number |  |
| `quote.USD.total_market_cap` | number |  |
| `quote.USD.total_market_cap_yesterday` | number |  |
| `quote.USD.total_market_cap_yesterday_percentage_change` | number |  |
| `quote.USD.total_volume_24h` | number |  |
| `quote.USD.total_volume_24h_reported` | number |  |
| `quote.USD.total_volume_24h_yesterday` | number |  |
| `quote.USD.total_volume_24h_yesterday_percentage_change` | number |  |
| `stablecoin_24h_percentage_change` | number |  |
| `stablecoin_market_cap` | number |  |
| `stablecoin_volume_24h` | number |  |
| `stablecoin_volume_24h_reported` | number |  |
| `today_change_percent` | number |  |
| `today_incremental_crypto_number` | number |  |
| `total_crypto_dex_currencies` | number |  |
| `total_cryptocurrencies` | number |  |
| `total_exchanges` | number |  |
| `tracked_yearly_number.maxIncrementalDate` | date |  |
| `tracked_yearly_number.maxIncrementalNumber` | number |  |
| `tracked_yearly_number.minIncrementalDate` | date |  |
| `tracked_yearly_number.minIncrementalNumber` | number |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v1/global-metrics/quotes/latest` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-global-metrics.md) for the provider-specific parameters and requirements.

