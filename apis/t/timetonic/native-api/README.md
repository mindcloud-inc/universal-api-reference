# Timetonic: Native API Reference

A consolidated summary of Timetonic's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://timetonic.com/live/api/?doc
- **API base URL:** `https://timetonic.com/live/api.php`

## Authentication

### API Key

Authenticate TimeTonic API requests with user IDs and a Sesskey.

### Credentials

- **API Key:** `apiKey` · required
- **OAuth User ID:** `oauthUserId` · required · TimeTonic OAuth user ID used as the o_u request parameter.
- **User ID:** `userId` · required · TimeTonic user ID used as the u_c request parameter.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.timetonic.com/hc/en-001/articles/4402560131602-Creation-of-an-API-key-Sesskey)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. Response data is read from `userInfo`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Or Update Multiple Table Rows](actions/create-or-update-multiple-table-rows.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#createOrUpdateTableRows-doc) |
| [Create Or Update Table Row](actions/create-or-update-table-row.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#createOrUpdateTableRow-doc) |
| [Create Session Key](actions/create-session-key.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#createSesskey-doc) |
| [Delete Table Value Comments](actions/delete-table-value-comments.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#deleteTableValueComments-doc) |
| [Edit Table Value Comments](actions/edit-table-value-comments.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#editTableValueComments-doc) |
| [Get All Books Info](actions/get-all-books-info.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getAllBooks-doc) |
| [Get Book Info](actions/get-book-info.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getBookInfo-doc) |
| [Get Book Messages](actions/get-book-messages.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getBookMessages-doc) |
| [Get Book Tables](actions/get-book-tables.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getBookTables-doc) |
| [Get Images Media Files And Documents From URL](actions/get-images-media-files-and-documents-from-url.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#images-doc) |
| [Get Table Value Comments](actions/get-table-value-comments.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getTableValueComments-doc) |
| [Get Table Value Subset](actions/get-table-value-subset.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getTableValueSubset-doc) |
| [Get User Info](actions/get-user-info.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getUserInfo-doc) |
| [Get User Session Key](actions/get-user-session-key.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#getOrCreateSessKey-doc) |
| [Register Application](actions/register-application.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#createAppkey-doc) |
| [Register Or Update Push Notification](actions/register-or-update-push-notification.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#updatePushId-doc) |
| [Render Smart Text Field](actions/render-smart-text-field.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#renderSmartTextField-doc) |
| [Resumable Upload](actions/resumable-upload.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#resumableUpload-doc) |
| [Rollback Change On A Row](actions/rollback-change-on-a-row.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#rollBackBeforeChange-doc) |
| [Send Message](actions/send-message.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#sendMsg-doc) |
| [User Login](actions/user-login.md) | `POST` | [docs](https://timetonic.com/live/api.php?doc=#createOauthkey-doc) |
