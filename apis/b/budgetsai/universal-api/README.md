# <img src="https://images.mindcloud.co/apps/icons/budgetsai_1776279829658.png" alt="Budgets.ai logo" width="28" height="28"> Budgets.ai: Universal API

Lead generation and outbound sales platform covering enrichment, email discovery, campaigns, and email verification.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/budgetsai/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crm.budgets.ai
- **Vendor API docs:** https://crm.budgets.ai/dashboard/api-center/incoming

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/budgetsai/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&state=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET |  |

