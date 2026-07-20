# <img src="https://images.mindcloud.co/apps/icons/icon-144x144_1776976798896.png" alt="MindMe logo" width="28" height="28"> MindMe: Universal API

MindMe mobile marketing and account platform integration scaffold.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mindMe/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mindmemobile.com/
- **Vendor API docs:** https://www.mindmemobile.com/platform/app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Access Token](actions/get-access-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindMe/latest/actions/get-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | GET | Retrieves an access token from MindMe. |

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List CRM Calendar Activities](actions/list-crm-calendar-activities.md) | GET | Retrieves CRM calendar activities from MindMe. |

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Appointment](actions/create-crm-appointment.md) | POST | Creates a new CRM appointment in MindMe. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in MindMe. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from MindMe. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from MindMe. |
| [Update Campaign Routes](actions/update-campaign-routes.md) | PUT | Updates campaign routes in MindMe. |
| [Update Campaign Schedule](actions/update-campaign-schedule.md) | PUT | Updates a campaign schedule in MindMe. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List Inboxes](actions/list-inboxes.md) | GET | Retrieves inboxes from MindMe. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in MindMe. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from MindMe. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from MindMe. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from MindMe. |
| [List Contacts By List](actions/list-contacts-by-list.md) | GET | Retrieves contacts from a list in MindMe. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in MindMe. |
| [Update Contact Categories](actions/update-contact-categories.md) | PUT | Adds or removes contact categories in MindMe. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Transfer Conversation](actions/create-or-transfer-conversation.md) | POST | Creates or transfers a conversation in MindMe. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from MindMe. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a new custom field in MindMe. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from MindMe. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in MindMe. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from MindMe. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [List Media Files](actions/list-media-files.md) | GET | Retrieves media files from MindMe. |
| [Upload Media File](actions/upload-media-file.md) | POST | Uploads a media file to MindMe. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact List](actions/create-contact-list.md) | POST | Creates a new contact list in MindMe. |
| [Create Smart List](actions/create-smart-list.md) | POST | Creates a new smart list in MindMe. |
| [List Contact Lists](actions/list-contact-lists.md) | GET | Retrieves contact lists from MindMe. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Conversation Messages](actions/list-conversation-messages.md) | GET | Retrieves conversation messages from MindMe. |
| [Send Conversation Message](actions/send-conversation-message.md) | POST | Creates a new conversation message in MindMe. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST | Creates a new contact note in MindMe. |
| [List Contact Notes](actions/list-contact-notes.md) | GET | Retrieves contact notes from MindMe. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in MindMe. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from MindMe. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Task](actions/create-crm-task.md) | POST | Creates a new CRM task in MindMe. |
| [List CRM Tasks](actions/list-crm-tasks.md) | GET | Retrieves CRM tasks from MindMe. |

### Timezone Settings

| Action | Method | Description |
| --- | --- | --- |
| [List Time Zones](actions/list-time-zones.md) | GET | Retrieves time zones from MindMe. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts To Sequence](actions/add-contacts-to-sequence.md) | PUT | Adds contacts to a sequence in MindMe. |
| [Create Automation](actions/create-automation.md) | POST | Creates a new automation in MindMe. |
| [List Automations](actions/list-automations.md) | GET | Retrieves automations from MindMe. |
| [Update Automation Status](actions/update-automation-status.md) | PUT | Updates an automation status in MindMe. |

