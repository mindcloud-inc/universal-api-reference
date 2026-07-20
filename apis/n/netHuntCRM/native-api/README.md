# NetHunt CRM: Native API Reference

A consolidated summary of NetHunt CRM's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://nethunt.com/integration-api
- **API base URL:** `https://nethunt.com/api/v1/zapier`

## Authentication

### Basic Authentication

Use your NetHunt login email as the username and your personal NetHunt API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Email Address:** `emailAddress` · required · NetHunt login email used as the Basic-auth username.
- **API Key:** `apiKey` · required · Personal NetHunt API key generated in Settings > Apps and other integrations.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://nethunt.com/integration-api#authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Gmail Thread to Record](actions/add-gmail-thread-to-record.md) | `POST /actions/link-gmail-thread/:recordId` | [docs](https://nethunt.com/integration-api#link-gmail-thread) |
| [Create Record](actions/create-record.md) | `POST /actions/create-record/:folderId` | [docs](https://nethunt.com/integration-api#create-record) |
| [Create Record Call Log](actions/create-record-call-log.md) | `POST /actions/create-call-log/:recordId` | [docs](https://nethunt.com/integration-api#create-call-log) |
| [Create Record Comment](actions/create-record-comment.md) | `POST /actions/create-comment/:recordId` | [docs](https://nethunt.com/integration-api#create-comment) |
| [Delete Record](actions/delete-record.md) | `POST /actions/delete-record/:recordId` | [docs](https://nethunt.com/integration-api#delete-record) |
| [Find Recent Record Changes](actions/find-recent-record-changes.md) | `GET /triggers/record-change/:folderId` | [docs](https://nethunt.com/integration-api#record-change) |
| [Find Recently Created Record Comments](actions/find-recently-created-record-comments.md) | `GET /triggers/new-comment/:folderId` | [docs](https://nethunt.com/integration-api#new-comment) |
| [Find Recently Created Records](actions/find-recently-created-records.md) | `GET /triggers/new-record/:folderId` | [docs](https://nethunt.com/integration-api#new-record) |
| [Find Recently Updated Records](actions/find-recently-updated-records.md) | `GET /triggers/updated-record/:folderId` | [docs](https://nethunt.com/integration-api#updated-record) |
| [Find Records](actions/find-records.md) | `GET /searches/find-record/:folderId` | [docs](https://nethunt.com/integration-api#find-record) |
| [List Accessible Folders](actions/list-accessible-folders.md) | `GET /triggers/readable-folder` | [docs](https://nethunt.com/integration-api#readable-folder) |
| [List Folder Fields](actions/list-folder-fields.md) | `GET /triggers/folder-field/:folderId` | [docs](https://nethunt.com/integration-api#folder-field) |
| [List Writable Folders](actions/list-writable-folders.md) | `GET /triggers/writable-folder` | [docs](https://nethunt.com/integration-api#writable-folder) |
| [Update Record](actions/update-record.md) | `POST /actions/update-record/:recordId` | [docs](https://nethunt.com/integration-api#update-record) |
| [Verify Request Credentials](actions/verify-request-credentials.md) | `GET /triggers/auth-test` | [docs](https://nethunt.com/integration-api#auth-test) |
