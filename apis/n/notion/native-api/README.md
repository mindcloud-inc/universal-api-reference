# Notion: Native API Reference

A consolidated summary of Notion's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://developers.notion.com/reference
- **API base URL:** `https://api.notion.com/v1`

## Authentication

### OAuth2

Notion OAuth2 authentication

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.notion.com/v1/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.notion.com/v1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read content, update content, insert content, read comments, insert comments`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.notion.com/v1/oauth/token.

[Official authentication documentation](https://developers.notion.com/docs/authorization)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Notion-Version` | `2022-06-28` |

The next-page cursor is read from `next_cursor`.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–100). Use `start_cursor` in the query string as the pagination cursor.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Append Block Children](actions/append-block-children.md) | `PATCH /blocks/:block_id/children` | [docs](https://developers.notion.com/reference/patch-block-children) |
| [Complete File Upload](actions/complete-file-upload.md) | `POST /file_uploads/:file_upload_id/complete` | [docs](https://developers.notion.com/reference/complete-a-file-upload) |
| [Create Comment](actions/create-comment.md) | `POST /comments` | [docs](https://developers.notion.com/reference/create-a-comment) |
| [Create Data Source](actions/create-data-source.md) | `POST /data_sources` | [docs](https://developers.notion.com/reference/create-a-data-source) |
| [Create Database](actions/create-database.md) | `POST /databases` | [docs](https://developers.notion.com/reference/create-database) |
| [Create File Upload](actions/create-file-upload.md) | `POST /file_uploads` | [docs](https://developers.notion.com/reference/create-a-file-upload) |
| [Create Page](actions/create-page.md) | `POST /pages` | [docs](https://developers.notion.com/reference/post-page) |
| [Delete Block](actions/delete-block.md) | `DELETE /blocks/:block_id` | [docs](https://developers.notion.com/reference/delete-a-block) |
| [List Block Children](actions/list-block-children.md) | `GET /blocks/:block_id/children` | [docs](https://developers.notion.com/reference/get-block-children) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://developers.notion.com/reference/list-comments) |
| [List Data Source Templates](actions/list-data-source-templates.md) | `GET /data_sources/:data_source_id/templates` | [docs](https://developers.notion.com/reference/list-data-source-templates) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.notion.com/reference/get-users) |
| [Query Data Source](actions/query-data-source.md) | `POST /data_sources/:data_source_id/query` | [docs](https://developers.notion.com/reference/query-a-data-source) |
| [Retrieve Block](actions/retrieve-block.md) | `GET /blocks/:block_id` | [docs](https://developers.notion.com/reference/retrieve-a-block) |
| [Retrieve Bot User](actions/retrieve-bot-user.md) | `GET /users/me` | [docs](https://developers.notion.com/reference/get-self) |
| [Retrieve Data Source](actions/retrieve-data-source.md) | `GET /data_sources/:data_source_id` | [docs](https://developers.notion.com/reference/retrieve-a-data-source) |
| [Retrieve Data Source Template](actions/retrieve-data-source-template.md) | `GET /pages/:template_id` | [docs](https://developers.notion.com/reference/retrieve-a-page) |
| [Retrieve Database (Compatibility)](actions/retrieve-database-compatibility.md) | `GET /databases/:database_id` | [docs](https://developers.notion.com/reference/retrieve-a-database) |
| [Retrieve Page](actions/retrieve-page.md) | `GET /pages/:page_id` | [docs](https://developers.notion.com/reference/retrieve-a-page) |
| [Retrieve Page Property Item](actions/retrieve-page-property-item.md) | `GET /pages/:page_id/properties/:property_id` | [docs](https://developers.notion.com/reference/retrieve-a-page-property) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:user_id` | [docs](https://developers.notion.com/reference/get-user) |
| [Search](actions/search.md) | `POST /search` | [docs](https://developers.notion.com/reference/post-search) |
| [Send File Upload](actions/send-file-upload.md) | `POST /file_uploads/:file_upload_id/send` | [docs](https://developers.notion.com/reference/send-a-file-upload) |
| [Update Block](actions/update-block.md) | `PATCH /blocks/:block_id` | [docs](https://developers.notion.com/reference/update-a-block) |
| [Update Data Source](actions/update-data-source.md) | `PATCH /data_sources/:data_source_id` | [docs](https://developers.notion.com/reference/update-a-data-source) |
| [Update Database](actions/update-database.md) | `PATCH /databases/:database_id` | [docs](https://developers.notion.com/reference/update-database) |
| [Update Page](actions/update-page.md) | `PATCH /pages/:page_id` | [docs](https://developers.notion.com/reference/patch-page) |
