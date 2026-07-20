# <img src="https://images.mindcloud.co/apps/icons/favicon-support-automatebusiness-com-48x48_1776947432619.png" alt="Automate Sales CRM logo" width="28" height="28"> Automate Sales CRM: Universal API

Automate Sales CRM is a CRM platform from Automate Business with a public API-key lead capture surface and a documented Pabbly integration catalog.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/automateSalesCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://automatebusiness.com
- **Vendor API docs:** https://support.automatebusiness.com/en/category/automate-sales-crm-6px6fi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Create New Lead V2](actions/create-new-lead-v2.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/automateSalesCRM/latest/actions/create-new-lead-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

## Actions (1)

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create New Lead V2](actions/create-new-lead-v2.md) | POST | Creates a new lead in Automate Sales CRM. |

