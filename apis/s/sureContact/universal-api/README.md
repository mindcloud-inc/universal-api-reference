# <img src="https://images.mindcloud.co/apps/icons/sure-contact_1774883487922.png" alt="SureContact logo" width="28" height="28"> SureContact: Universal API

Manage contacts, campaigns, lists, and marketing automations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sureContact/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://surecontact.com
- **Vendor API docs:** https://api.surecontact.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Campaign](actions/duplicate-campaign.md) | POST | Creates a draft copy of a SureContact campaign. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a specific campaign from SureContact. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaign records from your SureContact account. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from SureContact. |
| [Find Contact by Email](actions/find-contact-by-email.md) | GET | Finds a contact in SureContact by email address. |
| [Find or Create Contact](actions/find-or-create-contact.md) | POST | Finds a contact in SureContact, or creates one if no match is found. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a specific contact from SureContact. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves saved contact records from SureContact. |
| [List Contacts for List](actions/list-contacts-for-list.md) | GET | Retrieves contacts in a specific SureContact list. |
| [List Contacts for Tag](actions/list-contacts-for-tag.md) | GET | Retrieves contacts assigned to a SureContact tag. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in SureContact. |
| [Update Contact Status](actions/update-contact-status.md) | PUT | Updates a contact's status in SureContact. |
| [Upsert Contact](actions/upsert-contact.md) | PUT | Creates or updates a contact in SureContact by email. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts to List](actions/add-contacts-to-list.md) | PUT | Adds contacts to an existing SureContact list. |
| [Copy List](actions/copy-list.md) | POST | Creates a copy of an existing SureContact list. |
| [Create List](actions/create-list.md) | POST | Creates a new list in SureContact. |
| [Get List](actions/get-list.md) | GET | Retrieves a specific list from SureContact. |
| [List Lists](actions/list-lists.md) | GET | Retrieves available contact lists from SureContact. |
| [Remove Contacts from List](actions/remove-contacts-from-list.md) | PUT | Removes contacts from an existing SureContact list. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in SureContact. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note for a SureContact contact. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes for a SureContact contact. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in SureContact. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Reports Overview](actions/get-reports-overview.md) | GET | Retrieves high-level reporting metrics from SureContact. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts to Tag](actions/add-contacts-to-tag.md) | PUT | Adds contacts to an existing SureContact tag. |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in SureContact. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from SureContact. |
| [List Tags](actions/list-tags.md) | GET | Retrieves available contact tags from SureContact. |
| [Remove Contacts from Tag](actions/remove-contacts-from-tag.md) | PUT | Removes contacts from an existing SureContact tag. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in SureContact. |

