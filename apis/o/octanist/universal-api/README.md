# <img src="https://images.mindcloud.co/apps/icons/octanist_1774449927969.png" alt="Octanist logo" width="28" height="28"> Octanist: Universal API

Access Octanist leads, conversion stats, ad spend reports, and API health checks from Octanist's public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/octanist/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://octanist.com
- **Vendor API docs:** https://octanist.com/docs/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Key](actions/check-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octanist/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad Spend](actions/get-ad-spend.md) | GET | Retrieves ad spend data from Octanist. |
| [Get Stats](actions/get-stats.md) | GET | Retrieves dashboard statistics from Octanist. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Octanist. |
| [Get Lead by ID](actions/get-lead-by-id.md) | GET | Retrieves a lead by ID from Octanist. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Octanist. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Octanist. |

### Utility

| Action | Method | Description |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | GET | Checks whether an Octanist API key is valid. |

