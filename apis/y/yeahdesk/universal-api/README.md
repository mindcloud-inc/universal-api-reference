# <img src="https://images.mindcloud.co/apps/icons/favicon-help-yeahdesk-ru-48x48_1776795421432.png" alt="Yeahdesk logo" width="28" height="28"> Yeahdesk: Universal API

Manage customer conversations and contacts across messaging, email, and phone

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yeahdesk/latest
- **Category:** Support / Ticketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yeahdesk.ru
- **Vendor API docs:** https://help.yeahdesk.ru/docs/for-developers/http-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yeahdesk/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List contacts](actions/list-contacts.md) | GET | Retrieves contacts from Yeahdesk using optional search filters. |

