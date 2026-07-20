# <img src="https://images.mindcloud.co/apps/icons/coincap-icon_1777052790575.png" alt="CoinCap logo" width="28" height="28"> CoinCap: Universal API

Real-time cryptocurrency market data from CoinCap API 3.0, including assets, exchanges, rates, markets, and historical pricing endpoints from the documented REST v3 contract.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coinCap/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coincap.io
- **Vendor API docs:** https://pro.coincap.io/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assets](actions/list-assets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from CoinCap. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from CoinCap. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [Get Rate](actions/get-rate.md) | GET | Retrieves a conversion rate from CoinCap. |
| [List Rates](actions/list-rates.md) | GET | Retrieves conversion rates from CoinCap. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Exchange](actions/get-exchange.md) | GET | Retrieves an exchange from CoinCap. |
| [List Exchanges](actions/list-exchanges.md) | GET | Retrieves exchanges from CoinCap. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset History](actions/get-asset-history.md) | GET | Retrieves historical data for an asset from CoinCap. |
| [Get Asset Market Cap History](actions/get-asset-market-cap-history.md) | GET | Retrieves market cap history for an asset from CoinCap. |
| [Get Asset Markets](actions/get-asset-markets.md) | GET | Retrieves markets for an asset from CoinCap. |
| [List Markets](actions/list-markets.md) | GET | Retrieves markets from CoinCap. |

