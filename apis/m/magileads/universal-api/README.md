# <img src="https://images.mindcloud.co/apps/icons/magileads-icon_1775681553005.png" alt="Magileads logo" width="28" height="28"> Magileads: Universal API

Magileads is a B2B prospecting and multichannel outreach platform for lead generation, contact management, and PRM workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/magileads/latest
- **Category:** Marketing
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.magileads.com
- **Vendor API docs:** https://api.magileads.net

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List PRM Statuses](actions/list-prm-statuses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-prm-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Blacklist

| Action | Method | Description |
| --- | --- | --- |
| [Create Blacklist](actions/create-blacklist.md) | POST | Creates a new blacklist in Magileads. |
| [Delete Blacklist](actions/delete-blacklist.md) | DELETE | Deletes an existing blacklist from Magileads. |
| [Get Blacklist](actions/get-blacklist.md) | GET | Retrieves a blacklist profile from Magileads. |
| [List Blacklists](actions/list-blacklists.md) | GET | Retrieves all available blacklists from Magileads. |
| [Update Blacklist](actions/update-blacklist.md) | PUT | Updates an existing blacklist in Magileads. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact In List](actions/create-contact-in-list.md) | POST | Imports a contact into a Magileads contact list. |
| [Delete Contact In List](actions/delete-contact-in-list.md) | DELETE | Deletes a contact from a Magileads contact list. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact profile from a Magileads contact list. |
| [List Contact List Contacts](actions/list-contact-list-contacts.md) | GET | Retrieves contacts from a Magileads contact list. |
| [Search Contact List Contacts](actions/search-contact-list-contacts.md) | GET | Finds contacts in a Magileads contact list by criteria. |
| [Update Contact In List](actions/update-contact-in-list.md) | PUT | Updates a contact in a Magileads contact list. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in Magileads. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from Magileads. |
| [Get Contact List](actions/get-contact-list.md) | GET | Retrieves a contact list profile from Magileads. |
| [List Contact List Names](actions/list-contact-list-names.md) | GET | Retrieves contact list IDs and names from Magileads. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves all contact lists from Magileads. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in Magileads. |

### Prm Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get PRM Contact](actions/get-prm-contact.md) | GET | Retrieves a PRM contact profile from Magileads. |
| [List PRM Contacts](actions/list-prm-contacts.md) | GET | Retrieves your PRM contacts from Magileads. |

### Prm Custom Status

| Action | Method | Description |
| --- | --- | --- |
| [Create PRM Custom Status](actions/create-prm-custom-status.md) | POST | Creates a new PRM custom status in Magileads. |
| [Delete PRM Custom Status](actions/delete-prm-custom-status.md) | DELETE | Deletes a custom PRM status from Magileads. |
| [List PRM Custom Statuses](actions/list-prm-custom-statuses.md) | GET | Retrieves PRM custom statuses from Magileads. |
| [Update PRM Custom Status](actions/update-prm-custom-status.md) | PUT | Updates an existing PRM custom status in Magileads. |

### Prm Nurturing

| Action | Method | Description |
| --- | --- | --- |
| [Create PRM Nurturing](actions/create-prm-nurturing.md) | POST | Creates a new PRM nurturing in Magileads. |
| [Delete PRM Nurturing](actions/delete-prm-nurturing.md) | DELETE | Deletes an existing PRM nurturing from Magileads. |
| [Get PRM Nurturing](actions/get-prm-nurturing.md) | GET | Retrieves a PRM nurturing from Magileads. |
| [List PRM Nurturings](actions/list-prm-nurturings.md) | GET | Retrieves your PRM nurturings from Magileads. |
| [Update PRM Nurturing](actions/update-prm-nurturing.md) | PUT | Updates an existing PRM nurturing in Magileads. |

### Prm Status

| Action | Method | Description |
| --- | --- | --- |
| [List PRM Statuses](actions/list-prm-statuses.md) | GET | Retrieves your PRM statuses from Magileads. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Magileads. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Magileads. |
| [List Tags](actions/list-tags.md) | GET | Retrieves all available tags from Magileads. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Magileads. |

