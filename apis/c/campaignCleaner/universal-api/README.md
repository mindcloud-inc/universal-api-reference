# <img src="https://images.mindcloud.co/apps/icons/campaigncleaner-favicon_1774981203329.png" alt="Campaign Cleaner logo" width="28" height="28"> Campaign Cleaner: Universal API

Campaign Cleaner helps teams sanitize, optimize, analyze, and retrieve HTML email campaigns for better deliverability and client compatibility.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/campaignCleaner/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://campaigncleaner.com
- **Vendor API docs:** https://docs.campaigncleaner.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes a campaign from Campaign Cleaner. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Campaign Cleaner. |
| [Get Campaign PDF Analysis](actions/get-campaign-pdf-analysis.md) | GET | Retrieves a campaign PDF analysis from Campaign Cleaner. |
| [Get Campaign Status](actions/get-campaign-status.md) | GET | Retrieves a campaign's status from Campaign Cleaner. |
| [Get Credits](actions/get-credits.md) | GET | Retrieves remaining credits from Campaign Cleaner. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Campaign Cleaner. |
| [Send Campaign](actions/send-campaign.md) | POST | Submits a campaign for processing in Campaign Cleaner. |

