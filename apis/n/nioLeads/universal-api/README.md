# <img src="https://images.mindcloud.co/apps/icons/nio-leads_1776088620784.png" alt="NioLeads logo" width="28" height="28"> NioLeads: Universal API

Find business emails and check NioLeads credit balance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nioLeads/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nioleads.com
- **Vendor API docs:** https://nioleads.com/apidoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nioLeads/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves your available credit balance from NioLeads. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | GET | Finds a business email in NioLeads by name and domain. |

