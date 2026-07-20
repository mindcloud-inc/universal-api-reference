# Formcrafts: Native API Reference

A consolidated summary of Formcrafts's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://formcrafts.com/help/developers/api-docs-v2
- **API base URL:** `https://api.formcrafts.com/v2`

## Authentication

### Basic Auth

Use your Formcrafts API key as the username and leave the password empty.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://formcrafts.com/help/developers/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100).

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get File Content](actions/get-file-content.md) | `GET /files/:id/content` | [docs](https://formcrafts.com/help/developers/api-docs-v2) |
| [Get Form](actions/get-form.md) | `GET /forms/:id` | [docs](https://formcrafts.com/help/developers/api-docs-v2) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://formcrafts.com/help/developers/api-docs-v2) |
| [List Form Responses](actions/list-form-responses.md) | `GET /forms/:id/responses` | [docs](https://formcrafts.com/help/developers/api-docs-v2) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://formcrafts.com/help/developers/api-docs-v2) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://formcrafts.com/help/developers/api-docs-v2) |
