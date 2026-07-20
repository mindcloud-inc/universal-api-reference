# <img src="https://images.mindcloud.co/apps/icons/favicon-getanewsletter-com-48x48_1776260536402.png" alt="Get a Newsletter logo" width="28" height="28"> Get a Newsletter: Universal API

Create, send, and analyze newsletters and subscriber data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/getANewsletter/latest
- **Category:** Communication / Email Communications
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getanewsletter.com
- **Vendor API docs:** https://api.getanewsletter.com/v3/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getANewsletter/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Lists contacts in Get a Newsletter. |

