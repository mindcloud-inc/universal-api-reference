# <img src="https://images.mindcloud.co/apps/icons/use-inbox_1776693472932.png" alt="UseINBOX logo" width="28" height="28"> UseINBOX: Universal API

Email marketing API for managing INBOX campaigns, senders, newsletters, contacts, contact lists, groups, custom fields, and segments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/useINBOX/latest
- **Category:** Communication / Email Communications
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.useinbox.com/
- **Vendor API docs:** https://developers.useinbox.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Campaigns](actions/get-all-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-all-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Get Token](actions/get-token.md) | GET | Retrieves an access token from UseINBOX. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign With Custom HTML](actions/create-campaign-with-custom-html.md) | POST | Creates a campaign from custom HTML in UseINBOX. |
| [Create Campaign With Newsletter](actions/create-campaign-with-newsletter.md) | POST | Creates a campaign from a newsletter in UseINBOX. |
| [Get All Campaigns](actions/get-all-campaigns.md) | GET | Retrieves campaigns from UseINBOX. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from UseINBOX. |

### Contact Lists

| Action | Method | Description |
| --- | --- | --- |
| [Add Single Contact To List](actions/add-single-contact-to-list.md) | POST | Adds a contact to a list in UseINBOX. |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a contact list in UseINBOX. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from UseINBOX. |
| [Delete Single Contact From List](actions/delete-single-contact-from-list.md) | DELETE | Deletes a contact from a list in UseINBOX. |
| [Get All Contact Lists](actions/get-all-contact-lists.md) | GET | Retrieves contact lists from UseINBOX. |
| [Get Contact Import Status](actions/get-contact-import-status.md) | GET | Retrieves contact import status from UseINBOX. |
| [Import Contacts To List](actions/import-contacts-to-list.md) | POST | Imports contacts into a list in UseINBOX. |
| [Replace Contact List](actions/replace-contact-list.md) | PUT | Replaces an existing contact list in UseINBOX. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in UseINBOX. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Change Contact Status](actions/change-contact-status.md) | PUT | Updates a contact's status in UseINBOX. |
| [Get All Contacts](actions/get-all-contacts.md) | GET | Retrieves contacts from UseINBOX. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from UseINBOX. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in UseINBOX. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a custom field in UseINBOX. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from UseINBOX. |
| [Get All Custom Fields](actions/get-all-custom-fields.md) | GET | Retrieves custom fields from UseINBOX. |
| [Replace Custom Field](actions/replace-custom-field.md) | PUT | Replaces an existing custom field in UseINBOX. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in UseINBOX. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a group in UseINBOX. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from UseINBOX. |
| [Get All Groups](actions/get-all-groups.md) | GET | Retrieves groups from UseINBOX. |
| [Replace Group](actions/replace-group.md) | PUT | Replaces an existing group in UseINBOX. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in UseINBOX. |

### Newsletters

| Action | Method | Description |
| --- | --- | --- |
| [Create Newsletter](actions/create-newsletter.md) | POST | Creates a newsletter in UseINBOX. |
| [Delete Newsletter](actions/delete-newsletter.md) | DELETE | Deletes an existing newsletter from UseINBOX. |
| [Get All Newsletters](actions/get-all-newsletters.md) | GET | Retrieves newsletters from UseINBOX. |
| [Get Newsletter](actions/get-newsletter.md) | GET | Retrieves a newsletter from UseINBOX. |
| [Replace Newsletter](actions/replace-newsletter.md) | PUT | Replaces an existing newsletter in UseINBOX. |
| [Update Newsletter](actions/update-newsletter.md) | PUT | Updates an existing newsletter in UseINBOX. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from UseINBOX. |
| [Get All Segments](actions/get-all-segments.md) | GET | Retrieves segments from UseINBOX. |

### Senders

| Action | Method | Description |
| --- | --- | --- |
| [Create Sender](actions/create-sender.md) | POST | Creates a sender in UseINBOX. |
| [Delete Sender](actions/delete-sender.md) | DELETE | Deletes an existing sender from UseINBOX. |
| [Get All Senders](actions/get-all-senders.md) | GET | Retrieves senders from UseINBOX. |
| [Replace Sender](actions/replace-sender.md) | PUT | Replaces an existing sender in UseINBOX. |
| [Update Sender](actions/update-sender.md) | PUT | Updates an existing sender in UseINBOX. |

