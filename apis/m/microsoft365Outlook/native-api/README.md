# Microsoft 365 Outlook: Native API Reference

A consolidated summary of Microsoft 365 Outlook's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/graph/use-the-api
- **API base URL:** `https://graph.microsoft.com`

## Authentication

### OAuth 2.0

Connect to Microsoft 365 Outlook through Microsoft Graph delegated OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/common/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `User.Read Mail.ReadWrite Mail.Send offline_access`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/common/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/entra/identity-platform/v2-oauth2-auth-code-flow)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–999). Use `$skiptoken` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add File Attachment to Message](actions/add-file-attachment-to-message.md) | `POST /v1.0/me/messages/{{messageId}}/attachments` | [docs](https://learn.microsoft.com/en-us/graph/api/message-post-attachments?view=graph-rest-1.0) |
| [Create Draft Message](actions/create-draft-message.md) | `POST /v1.0/me/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/user-post-messages?view=graph-rest-1.0) |
| [Delete Message](actions/delete-message.md) | `DELETE /v1.0/me/messages/{{messageId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/message-delete?view=graph-rest-1.0) |
| [Forward Message](actions/forward-message.md) | `POST /v1.0/me/messages/{{messageId}}/forward` | [docs](https://learn.microsoft.com/en-us/graph/api/message-forward?view=graph-rest-1.0) |
| [Get Message](actions/get-message.md) | `GET /v1.0/me/messages/{{messageId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/message-get?view=graph-rest-1.0) |
| [Get Message Attachment](actions/get-message-attachment.md) | `GET /v1.0/me/messages/{{messageId}}/attachments/{{attachmentId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/attachment-get?view=graph-rest-1.0) |
| [List Child Mail Folders](actions/list-child-mail-folders.md) | `GET /v1.0/me/mailFolders/:mailFolderId/childFolders` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-childfolders?view=graph-rest-1.0) |
| [List Inbox Messages](actions/list-inbox-messages.md) | `GET /v1.0/me/mailFolders/inbox/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0) |
| [List Mail Folders](actions/list-mail-folders.md) | `GET /v1.0/me/mailFolders` | [docs](https://learn.microsoft.com/en-us/graph/api/user-list-mailfolders?view=graph-rest-1.0) |
| [List Message Attachments](actions/list-message-attachments.md) | `GET /v1.0/me/messages/{{messageId}}/attachments` | [docs](https://learn.microsoft.com/en-us/graph/api/message-list-attachments?view=graph-rest-1.0) |
| [List Messages in Folder](actions/list-messages-in-folder.md) | `GET /v1.0/me/mailFolders/{{mailFolderId}}/messages` | [docs](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0) |
| [Move Message](actions/move-message.md) | `POST /v1.0/me/messages/{{messageId}}/move` | [docs](https://learn.microsoft.com/en-us/graph/api/message-move?view=graph-rest-1.0) |
| [Reply All to Message](actions/reply-all-to-message.md) | `POST /v1.0/me/messages/{{messageId}}/replyAll` | [docs](https://learn.microsoft.com/en-us/graph/api/message-replyall?view=graph-rest-1.0) |
| [Reply to Message](actions/reply-to-message.md) | `POST /v1.0/me/messages/{{messageId}}/reply` | [docs](https://learn.microsoft.com/en-us/graph/api/message-reply?view=graph-rest-1.0) |
| [Send Draft Message](actions/send-draft-message.md) | `POST /v1.0/me/messages/{{messageId}}/send` | [docs](https://learn.microsoft.com/en-us/graph/api/message-send?view=graph-rest-1.0) |
| [Send Mail](actions/send-mail.md) | `POST /v1.0/me/sendMail` | [docs](https://learn.microsoft.com/en-us/graph/api/user-sendmail?view=graph-rest-1.0) |
| [Update Draft Message](actions/update-draft-message.md) | `PATCH /v1.0/me/messages/{{messageId}}` | [docs](https://learn.microsoft.com/en-us/graph/api/message-update?view=graph-rest-1.0) |
