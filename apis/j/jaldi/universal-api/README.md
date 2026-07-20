# <img src="https://images.mindcloud.co/apps/icons/jaldi_1774619155517.png" alt="Jaldi logo" width="28" height="28"> Jaldi: Universal API

Manage Jaldi lead campaigns and send or retrieve leads through Jaldi webhook APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jaldi/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jalditech.com
- **Vendor API docs:** https://jalditech.com/support/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Leads](actions/list-leads.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Jaldi. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Jaldi. |

