# <img src="https://images.mindcloud.co/apps/icons/fireberry_1771620751079.png" alt="Fireberry logo" width="28" height="28"> Fireberry: Universal API

Manage sales, marketing, service, and operations in one CRM.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fireberry/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://developers.fireberry.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireberry/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves all contact records from Fireberry. |

