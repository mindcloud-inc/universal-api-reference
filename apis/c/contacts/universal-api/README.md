# <img src="https://images.mindcloud.co/apps/icons/815b880eed83e2e1f1422f49fc5af4cf24b7e075_1775249300880.png" alt="Contacts+ logo" width="28" height="28"> Contacts+: Universal API

Manage contacts, tags, teams, and contact photos

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/contacts/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.contactsplus.com/
- **Vendor API docs:** https://www.contactsplus.com/developers/contacts-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves current account details from Contacts+. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Contacts+. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Contacts+. |
| [List Contacts by ID](actions/list-contacts-by-id.md) | GET | Retrieves contacts from Contacts+ by ID. |
| [Manage Contact Tags](actions/manage-contact-tags.md) | PUT | Adds or removes tags on Contacts+ contacts. |
| [Scroll Contacts](actions/scroll-contacts.md) | GET | Retrieves contacts from Contacts+ using a scroll cursor. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Contacts+ by search query. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Contacts+. |
| [Upload Contact Photo](actions/upload-contact-photo.md) | PUT | Uploads a photo for an existing Contacts+ contact. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Contacts+. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Contacts+. |
| [List Tags by ID](actions/list-tags-by-id.md) | GET | Retrieves tags from Contacts+ by ID. |
| [Scroll Tags](actions/scroll-tags.md) | GET | Retrieves tags from Contacts+ using a scroll cursor. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Contacts+. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves available team details from Contacts+. |

