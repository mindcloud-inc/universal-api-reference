# <img src="https://images.mindcloud.co/apps/icons/aero-leads_1775138869264.png" alt="AeroLeads logo" width="28" height="28"> AeroLeads: Universal API

AeroLeads is a B2B lead generation platform used to find business contact details and export prospects to CRM tools.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aeroLeads/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aeroleads.com
- **Vendor API docs:** https://aeroleads.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Email](actions/get-company-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aeroLeads/latest/actions/get-company-email?connectionId=$CONNECTION_ID&firstName=John&lastName=Doe&company=Acme%20Inc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Email](actions/get-company-email.md) | GET |  |
| [Get LinkedIn Details](actions/get-linked-in-details.md) | GET |  |

