# <img src="https://images.mindcloud.co/apps/icons/favicon-developers-weeek-net-48x48_1776696359525.png" alt="WEEEK logo" width="28" height="28"> WEEEK: Universal API

WEEEK public API access for CRM contacts and organizations using a workspace access token.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wEEEK/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weeek.net/
- **Vendor API docs:** https://developers.weeek.net/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEEEK/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST |  |
| [Delete Organization](actions/delete-organization.md) | DELETE |  |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |
| [Update Organization](actions/update-organization.md) | PUT |  |

