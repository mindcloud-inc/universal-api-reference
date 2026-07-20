# Microsoft 365: Native API Reference

A consolidated summary of Microsoft 365's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/overview
- **REST (skip pagination) base URL:** `https://graph.microsoft.com`
- **REST (nextLink pagination) base URL:** `https://graph.microsoft.com`
- **REST (deltaLink pagination) base URL:** `https://graph.microsoft.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access openid profile https://graph.microsoft.com/User.Read https://graph.microsoft.com/Mail.Read https://graph.microsoft.com/Mail.ReadWrite https://graph.microsoft.com/Mail.Send https://graph.microsoft.com/Calendars.ReadWrite https://graph.microsoft.com/Contacts.ReadWrite https://graph.microsoft.com/Files.ReadWrite.All https://graph.microsoft.com/Tasks.ReadWrite https://graph.microsoft.com/Tasks.ReadWrite.Shared https://graph.microsoft.com/Notes.ReadWrite https://graph.microsoft.com/User.ReadWrite.All https://graph.microsoft.com/Directory.ReadWrite.All`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

### REST (skip pagination)

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### REST (nextLink pagination)

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### REST (deltaLink pagination)

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

- **REST (skip pagination):** Use `$top` in the query string to set the page size (default 25; accepted range 1–100). Use `$skip` in the query string as the record offset.
- **REST (nextLink pagination):** Use `$top` in the query string to set the page size (default 25; accepted range 1–100). Follow the complete next-page URL returned by the API.
- **REST (deltaLink pagination):** Follow the complete next-page URL returned by the API.

## Endpoints (57 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Accept Event](actions/accept-event.md) | REST (skip pagination) | `POST /v1.0/me/events/:eventId/accept` | [docs](https://learn.microsoft.com/en-us/graph/api/event-accept?view=graph-rest-1.0) |
| [Create Contact](actions/create-contact.md) | REST (skip pagination) | `POST /v1.0/me/contacts` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-contacts?view=graph-rest-1.0) |
| [Create Draft Message](actions/create-draft-message.md) | REST (skip pagination) | `POST /v1.0/me/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-messages?view=graph-rest-1.0) |
| [Create Event](actions/create-event.md) | REST (skip pagination) | `POST /v1.0/me/events` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-events?view=graph-rest-1.0) |
| [Create Folder](actions/create-folder.md) | REST (skip pagination) | `POST /v1.0/me/drive/root:/{{folderPath}}:/children` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-post-children?view=graph-rest-1.0) |
| [Create Notebook](actions/create-notebook.md) | REST (skip pagination) | `POST /v1.0/me/onenote/notebooks` | [docs](https://learn.microsoft.com/en-us/graph/api/onenote-post-notebooks?view=graph-rest-1.0) |
| [Create Section](actions/create-section.md) | REST (skip pagination) | `POST /v1.0/me/onenote/notebooks/{{notebookId}}/sections` | [docs](https://learn.microsoft.com/en-us/graph/api/notebook-post-sections?view=graph-rest-1.0) |
| [Create Task](actions/create-task.md) | REST (skip pagination) | `POST /v1.0/me/todo/lists/{{taskListId}}/tasks` | [docs](https://learn.microsoft.com/en-us/graph/api/todotasklist-post-tasks?view=graph-rest-1.0) |
| [Create Workbook](actions/create-workbook.md) | REST (skip pagination) | `POST /v1.0/me/drive/root/children` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-post-children?view=graph-rest-1.0) |
| [Create Worksheet in Workbook](actions/create-worksheet-in-workbook.md) | REST (skip pagination) | `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheetcollection-add?view=graph-rest-1.0) |
| [Delete Contact](actions/delete-contact.md) | REST (skip pagination) | `DELETE /v1.0/me/contacts/{{contactId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/contact-delete?view=graph-rest-1.0) |
| [Delete Event](actions/delete-event.md) | REST (skip pagination) | `DELETE /v1.0/me/events/{{eventId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/event-delete?view=graph-rest-1.0) |
| [Delete Message](actions/delete-message.md) | REST (skip pagination) | `DELETE /v1.0/me/messages/{{messageId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/message-delete?view=graph-rest-1.0) |
| [Delete Task](actions/delete-task.md) | REST (skip pagination) | `DELETE /v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/todotask-delete?view=graph-rest-1.0) |
| [Download File](actions/download-file.md) | REST (skip pagination) | `GET /v1.0/me/drive/items/:itemId/content` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-get-content?view=graph-rest-1.0) |
| [Forward Message](actions/forward-message.md) | REST (skip pagination) | `POST /v1.0/me/messages/{{messageId}}/forward` | [docs](https://learn.microsoft.com/en-us/graph/api/message-forward?view=graph-rest-1.0) |
| [Get Contact](actions/get-contact.md) | REST (skip pagination) | `GET /v1.0/me/contacts/{{contactId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/contact-get?view=graph-rest-1.0) |
| [Get Event](actions/get-event.md) | REST (skip pagination) | `GET /v1.0/me/events/{{eventId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/event-get?view=graph-rest-1.0) |
| [Get Message](actions/get-message.md) | REST (skip pagination) | `GET /v1.0/me/messages/{{messageId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/message-get?view=graph-rest-1.0) |
| [Get Message Attachment](actions/get-message-attachment.md) | REST (skip pagination) | `GET /v1.0/me/messages/{{messageId}}/attachments/{{attachmentId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/attachment-get?view=graph-rest-1.0) |
| [Get My Drive](actions/get-my-drive.md) | REST (skip pagination) | `GET /v1.0/me/drive` | [docs](https://learn.microsoft.com/en-us/graph/api/drive-get?view=graph-rest-1.0) |
| [Get My Profile](actions/get-my-profile.md) | REST (skip pagination) | `GET /v1.0/me` | [docs](https://learn.microsoft.com/en-us/graph/api/user-get?view=graph-rest-1.0) |
| [Get Page](actions/get-page.md) | REST (skip pagination) | `GET /v1.0/me/onenote/pages/{{pageId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/page-get?view=graph-rest-1.0) |
| [Get Task](actions/get-task.md) | REST (skip pagination) | `GET /v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/todotask-get?view=graph-rest-1.0) |
| [Get Worksheet Used Range](actions/get-worksheet-used-range.md) | REST (skip pagination) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/usedRange()` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-usedrange?view=graph-rest-1.0) |
| [List Calendar View](actions/list-calendar-view.md) | REST (skip pagination) | `GET /v1.0/me/calendarView` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-calendarview?view=graph-rest-1.0) |
| [List Calendars](actions/list-calendars.md) | REST (skip pagination) | `GET /v1.0/me/calendars` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-calendars?view=graph-rest-1.0) |
| [List Child Mail Folders](actions/list-child-mail-folders.md) | REST (skip pagination) | `GET /v1.0/me/mailFolders/:mailFolderId/childFolders` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-childfolders?view=graph-rest-1.0) |
| [List Contacts](actions/list-contacts.md) | REST (skip pagination) | `GET /v1.0/me/contacts` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-contacts?view=graph-rest-1.0) |
| [List Entra Group Users](actions/list-entra-group-users.md) | REST (nextLink pagination) | `GET /v1.0/groups/:id/members` | [docs](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0) |
| [List Entra Groups](actions/list-entra-groups.md) | REST (nextLink pagination) | `GET /v1.0/groups` | [docs](https://learn.microsoft.com/en-us/graph/api/group-list?view=graph-rest-1.0) |
| [List Entra User Changes](actions/list-entra-user-changes.md) | REST (deltaLink pagination) | `GET /v1.0/users/delta` | [docs](https://learn.microsoft.com/en-us/graph/api/user-delta?view=graph-rest-1.0) |
| [List Entra Users](actions/list-entra-users.md) | REST (nextLink pagination) | `GET /v1.0/users` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list?view=graph-rest-1.0) |
| [List Events](actions/list-events.md) | REST (skip pagination) | `GET /v1.0/me/events` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-events?view=graph-rest-1.0) |
| [List Folder Items](actions/list-folder-items.md) | REST (skip pagination) | `GET /v1.0/me/drive/root:/{{folderPath}}:/children` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-list-children?view=graph-rest-1.0) |
| [List Inbox Messages](actions/list-inbox-messages.md) | REST (skip pagination) | `GET /v1.0/me/mailFolders/inbox/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0) |
| [List Mail Folders](actions/list-mail-folders.md) | REST (skip pagination) | `GET /v1.0/me/mailFolders` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-mailfolders?view=graph-rest-1.0) |
| [List Message Attachments](actions/list-message-attachments.md) | REST (skip pagination) | `GET /v1.0/me/messages/{{messageId}}/attachments` | [docs](https://learn.microsoft.com/en-us/graph/api/message-list-attachments?view=graph-rest-1.0) |
| [List Messages in Folder](actions/list-messages-in-folder.md) | REST (skip pagination) | `GET /v1.0/me/mailFolders/{{mailFolderId}}/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0) |
| [List My Drive Items](actions/list-my-drive-items.md) | REST (skip pagination) | `GET /v1.0/me/drive/root/children` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-list-children?view=graph-rest-1.0) |
| [List Notebooks](actions/list-notebooks.md) | REST (skip pagination) | `GET /v1.0/me/onenote/notebooks` | [docs](https://learn.microsoft.com/en-us/graph/api/onenote-list-notebooks?view=graph-rest-1.0) |
| [List Pages](actions/list-pages.md) | REST (skip pagination) | `GET /v1.0/me/onenote/pages` | [docs](https://learn.microsoft.com/en-us/graph/api/onenote-list-pages?view=graph-rest-1.0) |
| [List Sections](actions/list-sections.md) | REST (skip pagination) | `GET /v1.0/me/onenote/sections` | [docs](https://learn.microsoft.com/en-us/graph/api/onenote-list-sections?view=graph-rest-1.0) |
| [List Task Lists](actions/list-task-lists.md) | REST (skip pagination) | `GET /v1.0/me/todo/lists` | [docs](https://learn.microsoft.com/en-us/graph/api/todo-list-lists?view=graph-rest-1.0) |
| [List Tasks](actions/list-tasks.md) | REST (skip pagination) | `GET /v1.0/me/todo/lists/{{taskListId}}/tasks` | [docs](https://learn.microsoft.com/en-us/graph/api/todotasklist-list-tasks?view=graph-rest-1.0) |
| [List Worksheets](actions/list-worksheets.md) | REST (skip pagination) | `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets` | [docs](https://learn.microsoft.com/en-us/graph/api/worksheet-list?view=graph-rest-1.0) |
| [Move Message](actions/move-message.md) | REST (skip pagination) | `POST /v1.0/me/messages/{{messageId}}/move` | [docs](https://learn.microsoft.com/en-us/graph/api/message-move?view=graph-rest-1.0) |
| [Reply All to Message](actions/reply-all-to-message.md) | REST (skip pagination) | `POST /v1.0/me/messages/{{messageId}}/replyAll` | [docs](https://learn.microsoft.com/en-us/graph/api/message-replyall?view=graph-rest-1.0) |
| [Reply to Message](actions/reply-to-message.md) | REST (skip pagination) | `POST /v1.0/me/messages/{{messageId}}/reply` | [docs](https://learn.microsoft.com/en-us/graph/api/message-reply?view=graph-rest-1.0) |
| [Send Draft Message](actions/send-draft-message.md) | REST (skip pagination) | `POST /v1.0/me/messages/{{messageId}}/send` | [docs](https://learn.microsoft.com/en-us/graph/api/message-send?view=graph-rest-1.0) |
| [Send Mail](actions/send-mail.md) | REST (skip pagination) | `POST /v1.0/me/sendMail` | [docs](https://learn.microsoft.com/en-us/graph/api/user-sendmail?view=graph-rest-1.0) |
| [Update Contact](actions/update-contact.md) | REST (skip pagination) | `PATCH /v1.0/me/contacts/{{contactId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/contact-update?view=graph-rest-1.0) |
| [Update Draft Message](actions/update-draft-message.md) | REST (skip pagination) | `PATCH /v1.0/me/messages/{{messageId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/message-update?view=graph-rest-1.0) |
| [Update Event](actions/update-event.md) | REST (skip pagination) | `PATCH /v1.0/me/events/{{eventId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/event-update?view=graph-rest-1.0) |
| [Update Range Values](actions/update-range-values.md) | REST (skip pagination) | `PATCH /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')` | [docs](https://learn.microsoft.com/en-us/graph/api/range-update?view=graph-rest-1.0) |
| [Update Task](actions/update-task.md) | REST (skip pagination) | `PATCH /v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/todotask-update?view=graph-rest-1.0) |
| [Upload File](actions/upload-file.md) | REST (skip pagination) | `PUT /v1.0/me/drive/root\:/:folderPath/:fileName\:/content` | [docs](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0) |
