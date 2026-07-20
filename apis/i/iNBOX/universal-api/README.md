# <img src="https://images.mindcloud.co/apps/icons/i-nbox_1774379950545.png" alt="INBOX logo" width="28" height="28"> INBOX: Universal API

INBOX is an email marketing platform API for managing campaigns, newsletters, senders, contacts, contact lists, groups, custom fields, and segments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iNBOX/latest
- **Category:** Communication / Email Communications
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://useinbox.com/
- **Vendor API docs:** https://reference.useinbox.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Campaigns](actions/get-all-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/get-all-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign With Custom HTML](actions/create-campaign-with-custom-html.md) | POST | Creates a new INBOX campaign from custom HTML. |
| [Create Campaign With Newsletter](actions/create-campaign-with-newsletter.md) | POST | Creates a new INBOX campaign from a newsletter. |
| [Get All Campaigns](actions/get-all-campaigns.md) | GET | Retrieves all campaign records from INBOX. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves an existing campaign from INBOX. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Change Contact Status](actions/change-contact-status.md) | PUT | Updates a contact status in INBOX. |
| [Get All Contacts](actions/get-all-contacts.md) | GET | Retrieves all contact records from INBOX. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves an existing contact from INBOX. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in INBOX. |

### Contact List

| Action | Method | Description |
| --- | --- | --- |
| [Add Single Contact To List](actions/add-single-contact-to-list.md) | POST | Adds a contact to an INBOX contact list. |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in INBOX. |
| [Delete Contact List](actions/delete-contact-list.md) | DELETE | Deletes an existing contact list from INBOX. |
| [Delete Single Contact From List](actions/delete-single-contact-from-list.md) | DELETE | Removes a contact from an INBOX contact list. |
| [Get All Contact Lists](actions/get-all-contact-lists.md) | GET | Retrieves all contact lists from INBOX. |
| [Replace Contact List](actions/replace-contact-list.md) | PUT | Replaces an existing contact list in INBOX. |
| [Update Contact List](actions/update-contact-list.md) | PUT | Updates an existing contact list in INBOX. |

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in INBOX. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes an existing custom field from INBOX. |
| [Get All Custom Fields](actions/get-all-custom-fields.md) | GET | Retrieves all custom fields from INBOX. |
| [Replace Custom Field](actions/replace-custom-field.md) | PUT | Replaces an existing custom field in INBOX. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates an existing custom field in INBOX. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in INBOX. |
| [Delete Groups](actions/delete-groups.md) | DELETE | Deletes an existing group from INBOX. |
| [Get All Groups](actions/get-all-groups.md) | GET | Retrieves all group records from INBOX. |
| [Replace Group](actions/replace-group.md) | PUT | Replaces an existing group in INBOX. |
| [Update Groups](actions/update-groups.md) | PUT | Updates an existing group in INBOX. |

### Import Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Import Status](actions/get-import-status.md) | GET | Retrieves an import job status from INBOX. |
| [Import Contacts To List](actions/import-contacts-to-list.md) | POST | Imports contacts into an INBOX contact list. |

### Newsletter

| Action | Method | Description |
| --- | --- | --- |
| [Create Newsletter](actions/create-newsletter.md) | POST | Creates a new newsletter in INBOX. |
| [Delete Newsletter](actions/delete-newsletter.md) | DELETE | Deletes an existing newsletter from INBOX. |
| [Get All Newsletters](actions/get-all-newsletters.md) | GET | Retrieves all newsletter records from INBOX. |
| [Get Newsletter](actions/get-newsletter.md) | GET | Retrieves an existing newsletter from INBOX. |
| [Replace Newsletter](actions/replace-newsletter.md) | PUT | Replaces an existing newsletter in INBOX. |
| [Update Newsletter](actions/update-newsletter.md) | PUT | Updates an existing newsletter in INBOX. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from INBOX. |
| [Get All Segments](actions/get-all-segments.md) | GET | Retrieves all segment records from INBOX. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [Create Sender](actions/create-sender.md) | POST | Creates a new sender in INBOX. |
| [Delete Sender](actions/delete-sender.md) | DELETE | Deletes an existing sender from INBOX. |
| [Get All Senders](actions/get-all-senders.md) | GET | Retrieves all sender records from INBOX. |
| [Replace Sender](actions/replace-sender.md) | PUT | Replaces an existing sender in INBOX. |
| [Update Sender](actions/update-sender.md) | PUT | Updates an existing sender in INBOX. |

