# <img src="https://images.mindcloud.co/apps/icons/tg-booster_1776453229642.png" alt="TgBooster logo" width="28" height="28"> TgBooster: Universal API

Manage Telegram Ads cabinets, campaigns, and reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tgBooster/latest
- **Category:** Marketing / Advertising
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tgbooster.ru
- **Vendor API docs:** https://tgbooster.gitbook.io/tgbooster/api/api-metody

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Cabinets](actions/list-cabinets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-cabinets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Ad Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from a specific TgBooster cabinet. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Reports](actions/get-reports.md) | GET | Retrieves custom campaign reports from a TgBooster cabinet. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Cabinets](actions/list-cabinets.md) | GET | Retrieves Telegram Ads cabinets from TgBooster. |

