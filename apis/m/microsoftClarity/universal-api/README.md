# <img src="https://images.mindcloud.co/apps/icons/cd03dbb0-314d-4fac-bcd8-194045109a82-2_1774283950263.png" alt="Microsoft Clarity logo" width="28" height="28"> Microsoft Clarity: Universal API

Export recent Microsoft Clarity dashboard insights for traffic, engagement, devices, browsers, URLs, and campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftClarity/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://clarity.microsoft.com/
- **Vendor API docs:** https://learn.microsoft.com/en-us/clarity/setup-and-installation/clarity-data-export-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project Live Insights](actions/get-project-live-insights.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftClarity/latest/actions/get-project-live-insights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Project Live Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Live Insights](actions/get-project-live-insights.md) | GET | Retrieves project live insights from Microsoft Clarity. |

