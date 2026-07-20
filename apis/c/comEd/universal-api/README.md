# <img src="https://images.mindcloud.co/apps/icons/com-ed_1782741477391.png" alt="ComEd logo" width="28" height="28"> ComEd: Universal API

Track ComEd hourly and 5-minute electricity prices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/comEd/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hourlypricing.comed.com/
- **Vendor API docs:** https://hourlypricing.comed.com/hp-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Hour Average](actions/get-current-hour-average.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comEd/latest/actions/get-current-hour-average?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### 5-minute Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest 5-Minute Prices](actions/get-latest5-minute-prices.md) | GET | Retrieves the latest 5-minute prices from ComEd. |
| [Get 5-Minute Prices By Time Range](actions/get5-minute-prices-by-time-range.md) | GET | Retrieves 5-minute prices from ComEd for a time range. |

### Current Hour Average Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Hour Average](actions/get-current-hour-average.md) | GET | Retrieves the current hour average price from ComEd. |

