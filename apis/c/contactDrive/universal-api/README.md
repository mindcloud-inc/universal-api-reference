# <img src="https://images.mindcloud.co/apps/icons/contact-drive_1774886199140.png" alt="ContactDrive logo" width="28" height="28"> ContactDrive: Universal API

Manage contacts, segment audiences, and track relationships in ContactDrive

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/contactDrive/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.contactdrive.io
- **Vendor API docs:** https://help.contactdrive.io/article/16-api-v1

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactDrive/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Contact](actions/create-or-update-contact.md) | PUT |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Retrieve Contact](actions/retrieve-contact.md) | GET |  |

