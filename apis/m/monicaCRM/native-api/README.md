# Monica CRM: Native API Reference

A consolidated summary of Monica CRM's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.monicahq.com/api
- **API base URL:** `https://app.monicahq.com/api`

## Authentication

### API Key

Monica personal access token

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.monicahq.com/api)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity Type](actions/create-activity-type.md) | `POST /activitytypes` | [docs](https://www.monicahq.com/api/activitytypes) |
| [Create Contact Field Type](actions/create-contact-field-type.md) | `POST /contactfieldtypes` | [docs](https://www.monicahq.com/api/contactfieldtypes) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://www.monicahq.com/api/conversations) |
| [Delete Activity Type](actions/delete-activity-type.md) | `DELETE /activitytypes/:activityTypeId` | [docs](https://www.monicahq.com/api/activitytypes) |
| [Delete Contact Field Type](actions/delete-contact-field-type.md) | `DELETE /contactfieldtypes/:contactFieldTypeId` | [docs](https://www.monicahq.com/api/contactfieldtypes) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /conversations/:conversationId` | [docs](https://www.monicahq.com/api/conversations) |
| [Get Activity Type](actions/get-activity-type.md) | `GET /activitytypes/:activityTypeId` | [docs](https://www.monicahq.com/api/activitytypes) |
| [Get Call](actions/get-call.md) | `GET /calls/:callId` | [docs](https://www.monicahq.com/api/calls) |
| [Get Contact Field Type](actions/get-contact-field-type.md) | `GET /contactfieldtypes/:contactFieldTypeId` | [docs](https://www.monicahq.com/api/contactfieldtypes) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:conversationId` | [docs](https://www.monicahq.com/api/conversations) |
| [Get Gift](actions/get-gift.md) | `GET /gifts/:giftId` | [docs](https://www.monicahq.com/api/gifts) |
| [Get Journal Entry](actions/get-journal-entry.md) | `GET /journal/:journalEntryId` | [docs](https://www.monicahq.com/api/journal) |
| [Get Me](actions/get-me.md) | `GET /me` | [docs](https://www.monicahq.com/api) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tagId` | [docs](https://www.monicahq.com/api/tags) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://www.monicahq.com/api/activities) |
| [List Activity Types](actions/list-activity-types.md) | `GET /activitytypes` | [docs](https://www.monicahq.com/api/activitytypes) |
| [List Calls](actions/list-calls.md) | `GET /calls` | [docs](https://www.monicahq.com/api/calls) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://www.monicahq.com/api/companies) |
| [List Contact Field Types](actions/list-contact-field-types.md) | `GET /contactfieldtypes` | [docs](https://www.monicahq.com/api/contactfieldtypes) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://www.monicahq.com/api/contacts) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://www.monicahq.com/api/conversations) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://www.monicahq.com/api/documents) |
| [List Gifts](actions/list-gifts.md) | `GET /gifts` | [docs](https://www.monicahq.com/api/gifts) |
| [List Journal Entries](actions/list-journal-entries.md) | `GET /journal` | [docs](https://www.monicahq.com/api/journal) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://www.monicahq.com/api/notes) |
| [List Reminders](actions/list-reminders.md) | `GET /reminders` | [docs](https://www.monicahq.com/api/reminders) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://www.monicahq.com/api/tags) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://www.monicahq.com/api/tasks) |
| [Update Activity Type](actions/update-activity-type.md) | `PUT /activitytypes/:activityTypeId` | [docs](https://www.monicahq.com/api/activitytypes) |
| [Update Contact Field Type](actions/update-contact-field-type.md) | `PUT /contactfieldtypes/:contactFieldTypeId` | [docs](https://www.monicahq.com/api/contactfieldtypes) |
| [Update Conversation](actions/update-conversation.md) | `PUT /conversations/:conversationId` | [docs](https://www.monicahq.com/api/conversations) |
