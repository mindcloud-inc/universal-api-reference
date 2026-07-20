# <img src="https://images.mindcloud.co/apps/icons/25832602_1775771296191.png" alt="Monica CRM logo" width="28" height="28"> Monica CRM: Universal API

Personal CRM for contacts, activities, notes, reminders, tasks, companies, and documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/monicaCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.monicahq.com/
- **Vendor API docs:** https://www.monicahq.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Me](actions/get-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Monica CRM. |

### Calls

| Action | Method | Description |
| --- | --- | --- |
| [Get Call](actions/get-call.md) | GET | Retrieves a call from Monica CRM. |
| [List Calls](actions/list-calls.md) | GET | Retrieves calls from Monica CRM. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Monica CRM. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Monica CRM. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Monica CRM. |

### Journal Entries

| Action | Method | Description |
| --- | --- | --- |
| [Get Journal Entry](actions/get-journal-entry.md) | GET | Retrieves a journal entry from Monica CRM. |
| [List Journal Entries](actions/list-journal-entries.md) | GET | Retrieves journal entries from Monica CRM. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Monica CRM. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Reminders](actions/list-reminders.md) | GET | Retrieves reminders from Monica CRM. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Monica CRM. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Monica CRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Monica CRM. |

### Threads

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in Monica CRM. |
| [Delete Conversation](actions/delete-conversation.md) | DELETE | Deletes an existing conversation from Monica CRM. |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a conversation from Monica CRM. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations from Monica CRM. |
| [Update Conversation](actions/update-conversation.md) | PUT | Updates an existing conversation in Monica CRM. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Activity Type](actions/create-activity-type.md) | POST | Creates a new activity type in Monica CRM. |
| [Create Contact Field Type](actions/create-contact-field-type.md) | POST | Creates a new contact field type in Monica CRM. |
| [Delete Activity Type](actions/delete-activity-type.md) | DELETE | Deletes an existing activity type from Monica CRM. |
| [Delete Contact Field Type](actions/delete-contact-field-type.md) | DELETE | Deletes an existing contact field type from Monica CRM. |
| [Get Activity Type](actions/get-activity-type.md) | GET | Retrieves an activity type from Monica CRM. |
| [Get Contact Field Type](actions/get-contact-field-type.md) | GET | Retrieves a contact field type from Monica CRM. |
| [Get Gift](actions/get-gift.md) | GET | Retrieves a gift from Monica CRM. |
| [List Activity Types](actions/list-activity-types.md) | GET | Retrieves activity types from Monica CRM. |
| [List Contact Field Types](actions/list-contact-field-types.md) | GET | Retrieves contact field types from Monica CRM. |
| [List Gifts](actions/list-gifts.md) | GET | Retrieves gifts from Monica CRM. |
| [Update Activity Type](actions/update-activity-type.md) | PUT | Updates an existing activity type in Monica CRM. |
| [Update Contact Field Type](actions/update-contact-field-type.md) | PUT | Updates an existing contact field type in Monica CRM. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Me](actions/get-me.md) | GET | Retrieves your user profile from Monica CRM. |

