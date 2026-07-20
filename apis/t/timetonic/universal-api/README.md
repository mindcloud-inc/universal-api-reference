# <img src="https://images.mindcloud.co/apps/icons/id7vcw-mty-logos_1774465063203.jpeg" alt="Timetonic logo" width="28" height="28"> Timetonic: Universal API

Build collaborative business apps, centralize data, and automate workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timetonic/latest
- **Category:** IT Operations / Database
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://home.timetonic.com
- **Vendor API docs:** https://timetonic.com/live/api/?doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Register Application](actions/register-application.md) | POST | Creates a new application in Timetonic. |

### Book

| Action | Method | Description |
| --- | --- | --- |
| [Get All Books Info](actions/get-all-books-info.md) | GET | Retrieves information for all books from Timetonic. |
| [Get Book Info](actions/get-book-info.md) | GET | Retrieves information for a book from Timetonic. |

### Media File

| Action | Method | Description |
| --- | --- | --- |
| [Get Images Media Files And Documents From URL](actions/get-images-media-files-and-documents-from-url.md) | GET | Retrieves media files and documents from a URL in Timetonic. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Book Messages](actions/get-book-messages.md) | GET | Retrieves messages for a book from Timetonic. |
| [Send Message](actions/send-message.md) | POST | Creates a new message in Timetonic. |

### Oauth Key

| Action | Method | Description |
| --- | --- | --- |
| [User Login](actions/user-login.md) | POST | Creates an OAuth key in Timetonic for user login. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Resumable Upload](actions/resumable-upload.md) | POST | Creates a resumable upload in Timetonic. |

### Push Registration

| Action | Method | Description |
| --- | --- | --- |
| [Register Or Update Push Notification](actions/register-or-update-push-notification.md) | PUT | Creates or updates a push registration in Timetonic. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session Key](actions/create-session-key.md) | POST | Creates a session key in Timetonic. |
| [Get User Session Key](actions/get-user-session-key.md) | GET | Retrieves a user session key from Timetonic. |

### Smart Text Field

| Action | Method | Description |
| --- | --- | --- |
| [Render Smart Text Field](actions/render-smart-text-field.md) | GET | Retrieves rendered output for a smart text field from Timetonic. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Get Book Tables](actions/get-book-tables.md) | GET | Retrieves tables for a book from Timetonic. |

### Table Row

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Multiple Table Rows](actions/create-or-update-multiple-table-rows.md) | POST | Creates or updates multiple table rows in Timetonic. |
| [Create Or Update Table Row](actions/create-or-update-table-row.md) | POST | Creates or updates a table row in Timetonic. |
| [Get Table Value Subset](actions/get-table-value-subset.md) | GET | Retrieves a subset of table values from Timetonic. |
| [Rollback Change On A Row](actions/rollback-change-on-a-row.md) | PUT | Rolls back a row change in Timetonic. |

### Table Value Comment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Table Value Comments](actions/delete-table-value-comments.md) | DELETE | Deletes comments for a table value from Timetonic. |
| [Edit Table Value Comments](actions/edit-table-value-comments.md) | PUT | Updates comments for a table value in Timetonic. |
| [Get Table Value Comments](actions/get-table-value-comments.md) | GET | Retrieves comments for a table value from Timetonic. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves the current user information from Timetonic. |

