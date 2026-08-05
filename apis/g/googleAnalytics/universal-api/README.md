# <img src="https://images.mindcloud.co/apps/icons/como-criar-uma-propriedade-do-google-analytics-4_1758304207339.png" alt="Google Analytics logo" width="28" height="28"> Google Analytics: Universal API

Read Google Analytics 4 account, property, traffic, engagement, event, conversion, and ecommerce reporting data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleAnalytics/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://analytics.google.com/
- **Vendor API docs:** https://developers.google.com/analytics

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Account Summaries](actions/list-account-summaries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-account-summaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Analytics Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET |  |

### Analytics Account Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Account Summaries](actions/list-account-summaries.md) | GET |  |

### Analytics Property

| Action | Method | Description |
| --- | --- | --- |
| [List Properties](actions/list-properties.md) | GET |  |

### Analytics Property Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Property Metadata](actions/get-property-metadata.md) | GET |  |

### Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Custom Report](actions/run-custom-report.md) | GET |  |

### Conversions Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversions Report](actions/get-conversions-report.md) | GET |  |

### Device And Geography Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Device and Geography Report](actions/get-device-geography-report.md) | GET |  |

### Ecommerce Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Ecommerce Report](actions/get-ecommerce-report.md) | GET |  |

### Engagement Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Engagement Report](actions/get-engagement-report.md) | GET |  |

### Events Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Events and Key Events Report](actions/get-events-key-events-report.md) | GET |  |

### Funnel Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Funnel Report](actions/run-funnel-report.md) | GET |  |

### Landing Pages Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Landing Pages Report](actions/get-landing-pages-report.md) | GET |  |

### Pages Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Pages Report](actions/get-pages-report.md) | GET |  |

### Realtime Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Realtime Report](actions/run-realtime-report.md) | GET |  |

### Traffic Acquisition Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Traffic Acquisition Report](actions/get-traffic-acquisition-report.md) | GET |  |

