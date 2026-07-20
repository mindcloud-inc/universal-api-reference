# <img src="https://images.mindcloud.co/apps/icons/favicon_1777306759028.png" alt="HelloLeads logo" width="28" height="28"> HelloLeads: Universal API

HelloLeads CRM API for listing lead lists, listing leads, and creating leads with API key plus authorized email authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/helloLeads/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://helloleads.io/
- **Vendor API docs:** https://app.helloleads.io/index.php/app/account/layout#/apisettings

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lead Lists](actions/list-lead-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-lead-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST |  |
| [List Leads](actions/list-leads.md) | GET |  |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Lists](actions/list-lead-lists.md) | GET |  |

