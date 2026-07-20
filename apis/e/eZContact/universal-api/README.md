# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1775675266368.png" alt="EZContact logo" width="28" height="28"> EZContact: Universal API

WhatsApp automation platform with JSON-RPC API support for contacts, templates, and outbound messaging.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eZContact/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ezcontact.ai
- **Vendor API docs:** https://ezcontact.ai/en/integraciones/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Contacts](actions/search-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZContact/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Search Contacts](actions/search-contacts.md) | GET |  |

