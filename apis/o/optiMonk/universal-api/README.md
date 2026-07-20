# <img src="https://images.mindcloud.co/apps/icons/optimonk-icon-padded_1776692363564.png" alt="OptiMonk logo" width="28" height="28"> OptiMonk: Universal API

Access OptiMonk Public Reporting API data for account usage, campaigns, leads, and reporting metrics.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/optiMonk/latest
- **Category:** Marketing
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.optimonk.com
- **Vendor API docs:** https://support.optimonk.com/en/articles/11874795-optimonk-public-reporting-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves account details from OptiMonk. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from OptiMonk. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from OptiMonk. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from OptiMonk. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Report](actions/get-campaign-report.md) | GET | Retrieves a campaign report from OptiMonk. |
| [Get Overall Report](actions/get-overall-report.md) | GET | Retrieves the overall report from OptiMonk. |

