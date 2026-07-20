# <img src="https://images.mindcloud.co/apps/icons/images-2_1774025734261.jpeg" alt="PhoneBurner logo" width="28" height="28"> PhoneBurner: Universal API

PhoneBurner lets teams manage dial sessions, contacts, folders, tags, and related sales-calling data through the PhoneBurner REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/phoneBurner/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.phoneburner.com/
- **Vendor API docs:** https://www.phoneburner.com/developer/route_list

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phoneBurner/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in PhoneBurner. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from PhoneBurner. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from PhoneBurner. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a specific contact from PhoneBurner. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in PhoneBurner. |

