# <img src="https://images.mindcloud.co/apps/icons/google-contacts_1772575567011.png" alt="Google Contacts logo" width="28" height="28"> Google Contacts: Universal API

Organize contacts, update details, and manage contact photos

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleContacts/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://contacts.google.com
- **Vendor API docs:** https://developers.google.com/people/api/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Batch Get Contact Groups](actions/batch-get-contact-groups.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleContacts/latest/actions/batch-get-contact-groups?connectionId=$CONNECTION_ID&resourceNames=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Batch Create Contacts](actions/batch-create-contacts.md) | POST | Creates multiple new contacts in Google Contacts. |
| [Batch Delete Contacts](actions/batch-delete-contacts.md) | DELETE | Deletes multiple contacts from Google Contacts. |
| [Batch Get Contact Groups](actions/batch-get-contact-groups.md) | GET | Retrieves multiple contact groups from Google Contacts. |
| [Batch Get People](actions/batch-get-people.md) | GET | Retrieves multiple people from Google Contacts by resource name. |
| [Batch Update Contacts](actions/batch-update-contacts.md) | PUT | Updates multiple contacts in Google Contacts. |
| [Copy Other Contact To My Contacts Group](actions/copy-other-contact-to-my-contacts-group.md) | POST | Copies an other contact to My Contacts in Google Contacts. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Google Contacts. |
| [Create Contact Group](actions/create-contact-group.md) | POST | Creates a new contact group in Google Contacts. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Google Contacts. |
| [Delete Contact Group](actions/delete-contact-group.md) | DELETE | Deletes an existing contact group from Google Contacts. |
| [Delete Contact Photo](actions/delete-contact-photo.md) | DELETE | Deletes a contact photo from Google Contacts. |
| [Get Contact Group](actions/get-contact-group.md) | GET | Retrieves a contact group from Google Contacts. |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from Google Contacts. |
| [List Contact Groups](actions/list-contact-groups.md) | GET | Retrieves contact groups from Google Contacts. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves the authenticated user's contacts from Google Contacts. |
| [List Directory People](actions/list-directory-people.md) | GET | Retrieves directory people from the authenticated user's domain in Google Contacts. |
| [List Other Contacts](actions/list-other-contacts.md) | GET | Retrieves other contacts from Google Contacts. |
| [Modify Contact Group Members](actions/modify-contact-group-members.md) | PUT | Updates contact group membership in Google Contacts. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Google Contacts by search query. |
| [Search Directory People](actions/search-directory-people.md) | GET | Finds directory people in Google Contacts by prefix query. |
| [Search Other Contacts](actions/search-other-contacts.md) | GET | Finds other contacts in Google Contacts by search query. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Google Contacts. |
| [Update Contact Group](actions/update-contact-group.md) | PUT | Updates an existing contact group in Google Contacts. |
| [Update Contact Photo](actions/update-contact-photo.md) | PUT | Updates a contact photo in Google Contacts. |

