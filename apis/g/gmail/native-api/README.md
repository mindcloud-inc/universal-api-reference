# Google Mail: Native API Reference

A consolidated summary of Google Mail's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/gmail/api/reference/rest
- **API base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/gmail.labels https://www.googleapis.com/auth/gmail.modify https://www.googleapis.com/auth/pubsub openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile`.

Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/gmail/api/auth/about-auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `maxResults` in the query string to set the page size (default 100; accepted range 1–500). Use `pageToken` in the query string as the pagination cursor.

## Retry behavior

Wait 30000 ms before the first retry. Stop after 5 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Modify Emails](actions/batch-modify-emails.md) | `POST /messages/batchModify` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/batchModify) |
| [Create Draft](actions/create-draft.md) | `POST /drafts` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/create) |
| [Create Label](actions/create-label.md) | `POST /labels` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/create) |
| [Delete Draft](actions/delete-draft.md) | `DELETE /drafts/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/delete) |
| [Delete Label](actions/delete-label.md) | `DELETE /labels/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/delete) |
| [Get Draft](actions/get-draft.md) | `GET /drafts/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/get) |
| [Get Email](actions/get-email.md) | `GET /messages/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/get) |
| [Get Email Attachment](actions/get-email-attachment.md) | `GET /messages/:messageId/attachments/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages.attachments/get) |
| [Get Filter](actions/get-filter.md) | `GET /settings/filters/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.settings.filters/get) |
| [Get Label](actions/get-label.md) | `GET /labels/:labelId` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/get) |
| [Get Profile](actions/get-profile.md) | `GET /profile` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users/getProfile) |
| [Get Thread](actions/get-thread.md) | `GET /threads/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/get) |
| [Get Vacation Settings](actions/get-vacation-settings.md) | `GET /settings/vacation` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.settings/getVacation) |
| [Import Email](actions/import-email.md) | `POST /messages/import` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/import) |
| [Insert Email](actions/insert-email.md) | `POST /messages` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/insert) |
| [List Drafts](actions/list-drafts.md) | `GET /drafts` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/list) |
| [List Emails](actions/list-emails.md) | `GET /messages` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/list) |
| [List Filters](actions/list-filters.md) | `GET /settings/filters` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.settings.filters/list) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/list) |
| [List Threads](actions/list-threads.md) | `GET /threads` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/list) |
| [Modify Email Labels](actions/modify-email-labels.md) | `POST /messages/:id/modify` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/modify) |
| [Modify Thread Labels](actions/modify-thread-labels.md) | `POST /threads/:id/modify` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/modify) |
| [Patch Label](actions/patch-label.md) | `PATCH /labels/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/patch) |
| [Send Draft](actions/send-draft.md) | `POST /drafts/send` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/send) |
| [Send Email](actions/send-email.md) | `POST /messages/send` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/send) |
| [Start Mailbox Watch (Action)](actions/start-mailbox-watch-action.md) | `POST /watch` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users/watch) |
| [Stop Mailbox Watch](actions/stop-mailbox-watch.md) | `POST /stop` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users/stop) |
| [Trash Email](actions/trash-email.md) | `POST /messages/:id/trash` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/trash) |
| [Trash Thread](actions/trash-thread.md) | `POST /threads/:id/trash` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/trash) |
| [Untrash Email](actions/untrash-email.md) | `POST /messages/:id/untrash` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.messages/untrash) |
| [Untrash Thread](actions/untrash-thread.md) | `POST /threads/:id/untrash` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.threads/untrash) |
| [Update Draft](actions/update-draft.md) | `PUT /drafts/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.drafts/update) |
| [Update Label](actions/update-label.md) | `PUT /labels/:id` | [docs](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.labels/update) |
