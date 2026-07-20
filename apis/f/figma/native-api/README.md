# Figma: Native API Reference

A consolidated summary of Figma's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://developers.figma.com/docs/rest-api/
- **API base URL:** `https://api.figma.com/v1`

## Authentication

### OAuth 2.0

OAuth 2.0 Authorization Code flow for the Figma REST API.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.figma.com/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://api.figma.com/v1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `current_user:read file_comments:read file_comments:write file_content:read file_dev_resources:read file_dev_resources:write file_metadata:read file_versions:read library_assets:read library_content:read team_library_content:read webhooks:read webhooks:write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.figma.com/v1/oauth/token.

[Official authentication documentation](https://www.figma.com/developers/api#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100). Use `after` in the query string as the pagination cursor.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create File Comment](actions/create-file-comment.md) | `POST /files/:file_key/comments` | [docs](https://developers.figma.com/docs/rest-api/comments-endpoints/) |
| [Create Webhook](actions/create-webhook.md) | `POST https://api.figma.com/v2/webhooks` | [docs](https://developers.figma.com/docs/rest-api/webhooks-endpoints/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE https://api.figma.com/v2/webhooks/:webhook_id` | [docs](https://developers.figma.com/docs/rest-api/webhooks-endpoints/) |
| [Get Component](actions/get-component.md) | `GET /components/:key` | [docs](https://developers.figma.com/docs/rest-api/component-endpoints/) |
| [Get Component Set](actions/get-component-set.md) | `GET /component_sets/:key` | [docs](https://developers.figma.com/docs/rest-api/component-endpoints/) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://developers.figma.com/docs/rest-api/users-endpoints/) |
| [Get File](actions/get-file.md) | `GET /files/:key` | [docs](https://developers.figma.com/docs/rest-api/file-endpoints/) |
| [Get File Images](actions/get-file-images.md) | `GET /files/:key/images` | [docs](https://developers.figma.com/docs/rest-api/file-endpoints/) |
| [Get File Nodes](actions/get-file-nodes.md) | `GET /files/:key/nodes` | [docs](https://developers.figma.com/docs/rest-api/file-endpoints/) |
| [Get Local Variables](actions/get-local-variables.md) | `GET /files/:file_key/variables/local` | [docs](https://developers.figma.com/docs/rest-api/variables-endpoints/) |
| [Get Published Variables](actions/get-published-variables.md) | `GET /files/:file_key/variables/published` | [docs](https://developers.figma.com/docs/rest-api/variables-endpoints/) |
| [Get Rendered Images](actions/get-rendered-images.md) | `GET /images/:key` | [docs](https://developers.figma.com/docs/rest-api/file-endpoints/) |
| [Get Style](actions/get-style.md) | `GET /styles/:key` | [docs](https://developers.figma.com/docs/rest-api/component-endpoints/) |
| [List File Comments](actions/list-file-comments.md) | `GET /files/:key/comments` | [docs](https://developers.figma.com/docs/rest-api/comments-endpoints/) |
| [List File Component Sets](actions/list-file-component-sets.md) | `GET /files/:file_key/component_sets` | [docs](https://developers.figma.com/docs/rest-api/component-endpoints/) |
| [List File Components](actions/list-file-components.md) | `GET /files/:file_key/components` | [docs](https://developers.figma.com/docs/rest-api/component-endpoints/) |
| [List File Dev Resources](actions/list-file-dev-resources.md) | `GET https://api.figma.com/v1/files/:file_key/dev_resources` | [docs](https://developers.figma.com/docs/rest-api/dev-resources-endpoints/) |
| [List File Styles](actions/list-file-styles.md) | `GET /files/:file_key/styles` | [docs](https://developers.figma.com/docs/rest-api/component-endpoints/) |
| [List File Versions](actions/list-file-versions.md) | `GET /files/:key/versions` | [docs](https://developers.figma.com/docs/rest-api/version-history-endpoints/) |
| [List Webhooks](actions/list-webhooks.md) | `GET https://api.figma.com/v2/webhooks` | [docs](https://developers.figma.com/docs/rest-api/webhooks-endpoints/) |
| [Update Webhook](actions/update-webhook.md) | `PUT https://api.figma.com/v2/webhooks/:webhook_id` | [docs](https://developers.figma.com/docs/rest-api/webhooks-endpoints/) |
