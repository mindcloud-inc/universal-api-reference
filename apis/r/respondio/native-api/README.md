# respond.io: Native API Reference

A consolidated summary of respond.io's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.respond.io/
- **API base URL:** `https://api.respond.io/v2`

## Authentication

### API Key

Authenticate with a respond.io API token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1user/get?fromExportButton=true&snapshotType=http_operation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next`.

## Pagination

Use `limit` in the query string to set the page size. Use `cursorId` in the query string as the pagination cursor.

## Filtering

Send filters in the request body.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tags](actions/add-tags.md) | `POST /contact/:identifier/tag` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1tag/post?fromExportButton=true&snapshotType=http_operation) |
| [Assign Or Unassign Conversation](actions/assign-or-unassign-conversation.md) | `POST /contact/:identifier/conversation/assignee` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/conversation-api.yml/paths/~1contact~1%7Bidentifier%7D~1conversation~1assignee/post?fromExportButton=true&snapshotType=http_operation) |
| [Create Contact](actions/create-contact.md) | `POST /contact/:identifier` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D/post?fromExportButton=true&snapshotType=http_operation) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /space/custom_field` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1custom_field/post?fromExportButton=true&snapshotType=http_operation) |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /contact/create_or_update/:identifier` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1create_or_update~1%7Bidentifier%7D/post?fromExportButton=true&snapshotType=http_operation) |
| [Create Space Tag](actions/create-space-tag.md) | `POST /space/tag` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1tag/post?fromExportButton=true&snapshotType=http_operation) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/:identifier` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D/delete?fromExportButton=true&snapshotType=http_operation) |
| [Delete Space Tag](actions/delete-space-tag.md) | `DELETE /space/tag` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1tag/delete?fromExportButton=true&snapshotType=http_operation) |
| [Delete Tags](actions/delete-tags.md) | `DELETE /contact/:identifier/tag` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1tag/delete?fromExportButton=true&snapshotType=http_operation) |
| [Get Contact](actions/get-contact.md) | `GET /contact/:identifier` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D/get?fromExportButton=true&snapshotType=http_operation) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /space/custom_field/:id` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1custom_field~1%7Bid%7D/get?fromExportButton=true&snapshotType=http_operation) |
| [Get User](actions/get-user.md) | `GET /space/user/:id` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1user~1%7Bid%7D/get?fromExportButton=true&snapshotType=http_operation) |
| [List Channels](actions/list-channels.md) | `GET /space/channel` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1channel/get?fromExportButton=true&snapshotType=http_operation) |
| [List Closing Notes](actions/list-closing-notes.md) | `GET /space/closing_notes` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1closing_notes/get?fromExportButton=true&snapshotType=http_operation) |
| [List Contact Channels](actions/list-contact-channels.md) | `GET /contact/:identifier/channels` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1channels/get?fromExportButton=true&snapshotType=http_operation) |
| [List Contacts](actions/list-contacts.md) | `POST /contact/list` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1list/post?fromExportButton=true&snapshotType=http_operation) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /space/custom_field` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1custom_field/get?fromExportButton=true&snapshotType=http_operation) |
| [List Message Templates](actions/list-message-templates.md) | `GET /space/channel/:id/template` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1channel~1%7Bid%7D~1template/get?fromExportButton=true&snapshotType=http_operation) |
| [List Users](actions/list-users.md) | `GET /space/user` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1user/get?fromExportButton=true&snapshotType=http_operation) |
| [Merge Contacts](actions/merge-contacts.md) | `POST /contact/merge` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1merge/post?fromExportButton=true&snapshotType=http_operation) |
| [Open Or Close Conversation](actions/open-or-close-conversation.md) | `POST /contact/:identifier/conversation/status` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/conversation-api.yml/paths/~1contact~1%7Bidentifier%7D~1conversation~1status/post?fromExportButton=true&snapshotType=http_operation) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/:identifier` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D/put?fromExportButton=true&snapshotType=http_operation) |
| [Update Contact Lifecycle](actions/update-contact-lifecycle.md) | `POST /contact/:identifier/lifecycle/update` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D~1lifecycle~1update/post?fromExportButton=true&snapshotType=http_operation) |
| [Update Space Tag](actions/update-space-tag.md) | `PUT /space/tag` | [docs](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/space-api.yml/paths/~1space~1tag/put?fromExportButton=true&snapshotType=http_operation) |
