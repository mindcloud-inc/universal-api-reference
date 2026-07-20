# <img src="https://images.mindcloud.co/apps/icons/roboauditor-logo-300x130_1775071692503.png" alt="RoboAuditor logo" width="28" height="28"> RoboAuditor: Universal API

Embeddable white-label SEO audit and lead generation platform that helps teams capture and manage website audit leads.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/roboAuditor/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://siteauditor.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check URL Exists](actions/check-url-exists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/check-url-exists?connectionId=$CONNECTION_ID&websiteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | POST |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Integrations](actions/list-integrations.md) | GET |  |
| [Update Conversion Tracking](actions/update-conversion-tracking.md) | PUT |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Delete Domain Settings](actions/delete-domain-settings.md) | DELETE |  |
| [Export Leads](actions/export-leads.md) | GET |  |
| [Get Domain Settings](actions/get-domain-settings.md) | GET |  |
| [Get Lead Settings](actions/get-lead-settings.md) | GET |  |
| [Get Lead Token](actions/get-lead-token.md) | GET |  |
| [Import Leads](actions/import-leads.md) | POST |  |
| [List Blocked Leads](actions/list-blocked-leads.md) | GET |  |
| [List Leads](actions/list-leads.md) | GET |  |
| [Update Domain Settings](actions/update-domain-settings.md) | PUT |  |
| [Update Lead Settings](actions/update-lead-settings.md) | PUT |  |
| [Validate Domain Settings](actions/validate-domain-settings.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Check URL Exists](actions/check-url-exists.md) | GET |  |
| [Generate Report](actions/generate-report.md) | POST |  |
| [Get Report Settings](actions/get-report-settings.md) | GET |  |
| [Reset Report Settings](actions/reset-report-settings.md) | PUT |  |
| [Update Report Settings](actions/update-report-settings.md) | PUT |  |

