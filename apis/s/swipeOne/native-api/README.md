# Swipe One: Native API Reference

A consolidated summary of Swipe One's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://docs.swipeone.com/en/
- **API base URL:** `https://api.swipeone.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.swipeone.com/en/articles/10357358-workspace-settings)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /workspaces/:workspaceId/contacts` | [docs](https://docs.swipeone.com/en/articles/10545314-contacts#h_18dd8b78d4) |
| [Create Contact Property](actions/create-contact-property.md) | `POST /workspaces/:workspaceId/contact-properties` | [docs](https://docs.swipeone.com/en/articles/10540803-contact-properties#h_b218be703a) |
| [Create Event](actions/create-event.md) | `POST /workspaces/:workspaceId/events` | [docs](https://docs.swipeone.com/en/articles/10545660-events#h_29d9bc4044) |
| [Create Event Definition](actions/create-event-definition.md) | `POST /workspaces/:workspaceId/event-definitions` | [docs](https://docs.swipeone.com/en/articles/10358929-how-to-create-custom-event-definition-events#h_f97ca0d3fc) |
| [Create Note](actions/create-note.md) | `POST /contacts/:contactId/notes` | [docs](https://docs.swipeone.com/en/articles/10546101-notes#h_ba74b59a4f) |
| [Create Segment](actions/create-segment.md) | `POST /workspaces/:workspaceId/segments` | [docs](https://docs.swipeone.com/en/articles/10545714-segments#h_247c00ee31) |
| [Create Tag](actions/create-tag.md) | `POST /workspaces/:workspaceId/tags` | [docs](https://docs.swipeone.com/en/articles/10545829-tags#h_547ed7132f) |
| [Create Task](actions/create-task.md) | `POST /workspaces/:workspaceId/tasks` | [docs](https://docs.swipeone.com/en/articles/10546025-tasks#h_8e6a35db1f) |
| [Create Zapier Contact](actions/create-zapier-contact.md) | `POST /zapier/contact` | [docs](https://docs.swipeone.com/en/articles/10420029-swipeone-apis#h_4cf47da0d8) |
| [Create Zapier Event](actions/create-zapier-event.md) | `POST /zapier/event` | [docs](https://docs.swipeone.com/en/articles/10420029-swipeone-apis#h_6c762d18ff) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://docs.swipeone.com/en/articles/10545314-contacts#h_f4b3c88719) |
| [Get Contact Fields](actions/get-contact-fields.md) | `GET /zapier/fields` | [docs](https://docs.swipeone.com/en/articles/10420029-swipeone-apis#h_df3e8f9fd3) |
| [Get Contact Property](actions/get-contact-property.md) | `GET /contact-properties/:contactPropertyId` | [docs](https://docs.swipeone.com/en/articles/10540803-contact-properties#h_1071d9b27a) |
| [Get Make Event Properties](actions/get-make-event-properties.md) | `GET /make/events/:event` | [docs](https://docs.swipeone.com/en/articles/10429345-swipeone-make-com-apis#h_2646912b4c) |
| [Get Note](actions/get-note.md) | `GET /notes/:noteId` | [docs](https://docs.swipeone.com/en/articles/10546101-notes#h_c6e1bb09a1) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:segmentId` | [docs](https://docs.swipeone.com/en/articles/10545714-segments#h_195dca80d5) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tagId` | [docs](https://docs.swipeone.com/en/articles/10545829-tags#h_abdc4230b6) |
| [Get Task](actions/get-task.md) | `GET /tasks/:taskId` | [docs](https://docs.swipeone.com/en/articles/10546025-tasks#h_84c0b2fe74) |
| [Get Zapier Event Properties](actions/get-zapier-event-properties.md) | `GET /zapier/events/:event` | [docs](https://docs.swipeone.com/en/articles/10420029-swipeone-apis#h_4692d52af5) |
| [List Contact Events](actions/list-contact-events.md) | `GET /contacts/:contactId/events` | [docs](https://docs.swipeone.com/en/articles/10545660-events#h_3579944cc9) |
| [List Contact Notes](actions/list-contact-notes.md) | `GET /contacts/:contactId/notes` | [docs](https://docs.swipeone.com/en/articles/10546101-notes#h_84e41e006a) |
| [List Contact Properties](actions/list-contact-properties.md) | `GET /workspaces/:workspaceId/contact-properties` | [docs](https://docs.swipeone.com/en/articles/10540803-contact-properties#h_1db197abb9) |
| [List Contact Tasks](actions/list-contact-tasks.md) | `GET /workspaces/:workspaceId/contacts/:contactId/tasks` | [docs](https://docs.swipeone.com/en/articles/10546025-tasks#h_ac22398bff) |
| [List Contacts](actions/list-contacts.md) | `GET /workspaces/:workspaceId/contacts` | [docs](https://docs.swipeone.com/en/articles/10545314-contacts#h_8aa63bed28) |
| [List Make Events](actions/list-make-events.md) | `GET /make/events` | [docs](https://docs.swipeone.com/en/articles/10429345-swipeone-make-com-apis#h_476b302b1c) |
| [List Notes](actions/list-notes.md) | `GET /workspaces/:workspaceId/notes` | [docs](https://docs.swipeone.com/en/articles/10546101-notes#h_05759b3939) |
| [List Segment Contacts](actions/list-segment-contacts.md) | `GET /segments/:segmentId/contacts` | [docs](https://docs.swipeone.com/en/articles/10545714-segments#h_8dc591aa4e) |
| [List Segments](actions/list-segments.md) | `GET /workspaces/:workspaceId/segments` | [docs](https://docs.swipeone.com/en/articles/10545714-segments#h_23fd090102) |
| [List Tag Contacts](actions/list-tag-contacts.md) | `GET /tags/:tagId/contacts` | [docs](https://docs.swipeone.com/en/articles/10545829-tags#h_884fb7b948) |
| [List Tags](actions/list-tags.md) | `GET /workspaces/:workspaceId/tags` | [docs](https://docs.swipeone.com/en/articles/10545829-tags#h_db0e65aea0) |
| [List Tasks](actions/list-tasks.md) | `GET /workspaces/:workspaceId/tasks` | [docs](https://docs.swipeone.com/en/articles/10546025-tasks#h_6ad4d3fe4c) |
| [List Zapier Events](actions/list-zapier-events.md) | `GET /zapier/events` | [docs](https://docs.swipeone.com/en/articles/10420029-swipeone-apis#h_3f57589e90) |
| [Search Contacts](actions/search-contacts.md) | `POST /workspaces/:workspaceId/contacts/search` | [docs](https://docs.swipeone.com/en/articles/10545314-contacts#h_52c6526aef) |
| [Update Contact Tags](actions/update-contact-tags.md) | `POST /contacts/:contactId/tags` | [docs](https://docs.swipeone.com/en/articles/10545829-tags#h_9840d2c2ef) |
| [Update Note](actions/update-note.md) | `PATCH /notes/:noteId` | [docs](https://docs.swipeone.com/en/articles/10546101-notes#h_80ff056a23) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:taskId` | [docs](https://docs.swipeone.com/en/articles/10546025-tasks#h_38e3d525a6) |
