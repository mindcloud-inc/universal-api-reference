# <img src="https://images.mindcloud.co/apps/icons/whisky-hunter-icon_1776793988901.png" alt="Whisky Hunter logo" width="28" height="28"> Whisky Hunter: Universal API

Public Whisky Hunter API wrapper for online whisky auction aggregates, auction metadata, distillery metadata, and per-auction or per-distillery market data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/whiskyHunter/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://whiskyhunter.net/
- **Vendor API docs:** https://whiskyhunter.net/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Schema](actions/get-api-schema.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiskyHunter/latest/actions/get-api-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Api Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get API Schema](actions/get-api-schema.md) | GET | Retrieves the Whisky Hunter API schema. |

### Auction

| Action | Method | Description |
| --- | --- | --- |
| [List Auctions](actions/list-auctions.md) | GET | Retrieves online auction details from Whisky Hunter. |

### Auction Market Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Auction Market Data](actions/get-auction-market-data.md) | GET | Retrieves aggregated market data for one Whisky Hunter auction. |
| [List Auction Market Data](actions/list-auction-market-data.md) | GET | Retrieves aggregated online auction market data from Whisky Hunter. |

### Distillery

| Action | Method | Description |
| --- | --- | --- |
| [List Distilleries](actions/list-distilleries.md) | GET | Retrieves distillery details from Whisky Hunter. |

### Distillery Market Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Distillery Market Data](actions/get-distillery-market-data.md) | GET | Retrieves market data for one Whisky Hunter distillery. |

