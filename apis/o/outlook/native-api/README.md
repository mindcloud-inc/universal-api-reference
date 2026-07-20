# Outlook: Native API Reference

A consolidated summary of Outlook's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/api/resources/message
- **API base URL:** `https://graph.microsoft.com/v1.0`

## Authentication

### Microsoft OAuth2

Authorize Outlook Mail with Microsoft Graph delegated mailbox access for reading, sending, and draft/update/delete mail actions.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid profile email offline_access User.Read Mail.Read Mail.ReadWrite Mail.Send`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/graph/auth-v2-user)

## API conventions

Responses from this API use JSON. Response data is read from `value`.

## Pagination

Use `$top` in the query string to set the page size (default 10; accepted range 1–100).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Draft Message](actions/create-draft-message.md) | `POST /me/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-messages) |
| [Delete Message](actions/delete-message.md) | `DELETE /me/messages/:messageId` | [docs](https://learn.microsoft.com/en-us/graph/api/message-delete) |
| [Get Mail Folder](actions/get-mail-folder.md) | `GET /me/mailFolders/:folderId` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-get) |
| [Get Message](actions/get-message.md) | `GET /me/messages/:messageId` | [docs](https://learn.microsoft.com/en-us/graph/api/message-get) |
| [List Folder Messages](actions/list-folder-messages.md) | `GET /me/mailFolders/:folderId/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages) |
| [List Mail Folders](actions/list-mail-folders.md) | `GET /me/mailFolders` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-mailfolders) |
| [List Message Attachments](actions/list-message-attachments.md) | `GET /me/messages/:messageId/attachments` | [docs](https://learn.microsoft.com/en-us/graph/api/message-list-attachments) |
| [List Messages](actions/list-messages.md) | `GET /me/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-messages) |
| [Send Draft Message](actions/send-draft-message.md) | `POST /me/messages/:messageId/send` | [docs](https://learn.microsoft.com/en-us/graph/api/message-send) |
| [Send Mail](actions/send-mail.md) | `POST /me/sendMail` | [docs](https://learn.microsoft.com/en-us/graph/api/user-sendmail) |
| [Update Message](actions/update-message.md) | `PATCH /me/messages/:messageId` | [docs](https://learn.microsoft.com/en-us/graph/api/message-update) |
