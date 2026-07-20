# Zoho Mail: Native API Reference

A consolidated summary of Zoho Mail's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.zoho.com/mail/help/api/
- **API base URL:** `https://mail.zoho.com/api`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `ZohoMail.accounts.READ,ZohoMail.folders.ALL,ZohoMail.tags.ALL,ZohoMail.messages.ALL`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://www.zoho.com/accounts/protocol/oauth/web-server-applications.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–200). Use `start` in the query string as the record offset.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortorder`. Use `true` for ascending order and `false` for descending order. Only one sort field is accepted.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Labels To Emails](actions/apply-labels-to-emails.md) | `PUT /accounts/:accountId/updatemessage` | [docs](https://www.zoho.com/mail/help/api/add-tag-to-email.html) |
| [Archive Emails](actions/archive-emails.md) | `PUT /accounts/:accountId/updatemessage` | [docs](https://www.zoho.com/mail/help/api/put-archive-email.html) |
| [Create Folder](actions/create-folder.md) | `POST /accounts/:accountId/folders` | [docs](https://www.zoho.com/mail/help/api/post-create-new-folder.html) |
| [Create Label](actions/create-label.md) | `POST /accounts/:accountId/labels` | [docs](https://www.zoho.com/mail/help/api/post-create-new-label.html) |
| [Delete Email](actions/delete-email.md) | `DELETE /accounts/:accountId/folders/:folderId/messages/:messageId` | [docs](https://www.zoho.com/mail/help/api/delete-email.html) |
| [Download Attachment](actions/download-attachment.md) | `GET /accounts/:accountId/folders/:folderId/messages/:messageId/attachments/:attachmentId` | [docs](https://www.zoho.com/mail/help/api/get-attachment-content.html) |
| [Flag Emails](actions/flag-emails.md) | `PUT /accounts/:accountId/updatemessage` | [docs](https://www.zoho.com/mail/help/api/set-flag-for-email.html) |
| [Get Account Details](actions/get-account-details.md) | `GET /accounts/:accountId` | [docs](https://www.zoho.com/mail/help/api/get-user-account-details.html) |
| [Get Attachment Info](actions/get-attachment-info.md) | `GET /accounts/:accountId/folders/:folderId/messages/:messageId/attachmentinfo` | [docs](https://www.zoho.com/mail/help/api/get-attach-info.html) |
| [Get Email Content](actions/get-email-content.md) | `GET /accounts/:accountId/folders/:folderId/messages/:messageId/content` | [docs](https://www.zoho.com/mail/help/api/get-email-content.html) |
| [Get Email Metadata](actions/get-email-metadata.md) | `GET /accounts/:accountId/folders/:folderId/messages/:messageId/details` | [docs](https://www.zoho.com/mail/help/api/get-email-meta-data.html) |
| [Get Folder](actions/get-folder.md) | `GET /accounts/:accountId/folders/:folderId` | [docs](https://www.zoho.com/mail/help/api/get-single-folder-details.html) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://www.zoho.com/mail/help/api/get-all-users-accounts.html) |
| [List Emails](actions/list-emails.md) | `GET /accounts/:accountId/messages/view` | [docs](https://www.zoho.com/mail/help/api/get-emails-list.html) |
| [List Folders](actions/list-folders.md) | `GET /accounts/:accountId/folders` | [docs](https://www.zoho.com/mail/help/api/get-all-folder-details.html) |
| [List Labels](actions/list-labels.md) | `GET /accounts/:accountId/labels` | [docs](https://www.zoho.com/mail/help/api/get-all-label-details.html) |
| [Mark Emails Read](actions/mark-emails-read.md) | `PUT /accounts/:accountId/updatemessage` | [docs](https://www.zoho.com/mail/help/api/put-mark-email-as-read.html) |
| [Mark Emails Unread](actions/mark-emails-unread.md) | `PUT /accounts/:accountId/updatemessage` | [docs](https://www.zoho.com/mail/help/api/put-mark-email-as-unread.html) |
| [Move Emails](actions/move-emails.md) | `PUT /accounts/:accountId/updatemessage` | [docs](https://www.zoho.com/mail/help/api/move-email.html) |
| [Reply To Email](actions/reply-to-email.md) | `POST /accounts/:accountId/messages/:messageId` | [docs](https://www.zoho.com/mail/help/api/post-reply-to-an-email.html) |
| [Save Draft](actions/save-draft.md) | `POST /accounts/:accountId/messages` | [docs](https://www.zoho.com/mail/help/api/post-save-draft-template.html) |
| [Search Emails](actions/search-emails.md) | `GET /accounts/:accountId/messages/search` | [docs](https://www.zoho.com/mail/help/api/get-search-emails.html) |
| [Send Email](actions/send-email.md) | `POST /accounts/:accountId/messages` | [docs](https://www.zoho.com/mail/help/api/post-send-an-email.html) |
