# Pabbly Hook: Native API Reference

A consolidated summary of Pabbly Hook's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.pabbly.com/
- **API base URL:** `https://hook.pabbly.com`

## Authentication

### Basic Auth

Use your Pabbly Hook API Key as the username and Secret Key as the password for HTTP Basic authentication.

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

[Official authentication documentation](https://forum.pabbly.com/threads/what-is-pabbly-hook-api-and-secret-key.25709/)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | `POST /api/v1/connections` | [docs](https://apidocs.pabbly.com/) |
| [Create Folder](actions/create-folder.md) | `POST /api/v1/folders` | [docs](https://apidocs.pabbly.com/) |
| [Create Transformation](actions/create-transformation.md) | `POST /api/v1/transformations` | [docs](https://apidocs.pabbly.com/) |
| [Delete Connections](actions/delete-connections.md) | `DELETE /api/v1/connections` | [docs](https://apidocs.pabbly.com/) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /api/v1/folders/:folderId` | [docs](https://apidocs.pabbly.com/) |
| [Filter Connections](actions/filter-connections.md) | `GET /api/v1/connections` | [docs](https://apidocs.pabbly.com/) |
| [Filter Events](actions/filter-events.md) | `GET /api/v1/events` | [docs](https://apidocs.pabbly.com/) |
| [Filter Requests](actions/filter-requests.md) | `GET /api/v1/requests` | [docs](https://apidocs.pabbly.com/) |
| [Get All Folders](actions/get-all-folders.md) | `GET /api/v1/folders` | [docs](https://apidocs.pabbly.com/) |
| [Get All Transformations](actions/get-all-transformations.md) | `GET /api/v1/transformations/get-all/` | [docs](https://apidocs.pabbly.com/) |
| [Get Connection](actions/get-connection.md) | `GET /api/v1/connections/:connectionId` | [docs](https://apidocs.pabbly.com/) |
| [Get Transformation](actions/get-transformation.md) | `GET /api/v1/transformations/:transformationId` | [docs](https://apidocs.pabbly.com/) |
| [Move Connection To Folder](actions/move-connection-to-folder.md) | `PUT /api/v1/folders/move-connection` | [docs](https://apidocs.pabbly.com/) |
| [Rename Folder](actions/rename-folder.md) | `PUT /api/v1/folders/rename/:folderId` | [docs](https://apidocs.pabbly.com/) |
| [Retrieve All Events](actions/retrieve-all-events.md) | `GET /api/v1/events` | [docs](https://apidocs.pabbly.com/) |
| [Retrieve All Requests](actions/retrieve-all-requests.md) | `GET /api/v1/requests` | [docs](https://apidocs.pabbly.com/) |
| [Update Connection](actions/update-connection.md) | `PATCH /api/v1/connections/:connectionId` | [docs](https://apidocs.pabbly.com/) |
| [Update Transformation](actions/update-transformation.md) | `PUT /api/v1/transformations/:transformationId` | [docs](https://apidocs.pabbly.com/) |
