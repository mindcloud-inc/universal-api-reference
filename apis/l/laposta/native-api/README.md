# Laposta: Native API Reference

A consolidated summary of Laposta's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://api.laposta.nl/doc/index.en.php
- **API base URL:** `https://api.laposta.nl/v2`

## Authentication

### Basic Authentication

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

[Official authentication documentation](https://api.laposta.nl/doc/index.en.php)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | `POST /field` | [docs](https://api.laposta.nl/doc/index.en.php#fields) |
| [Create List](actions/create-list.md) | `POST /list` | [docs](https://api.laposta.nl/doc/index.en.php#lists) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /member` | [docs](https://api.laposta.nl/doc/index.en.php#members) |
| [Delete Field](actions/delete-field.md) | `DELETE /field/:fieldId` | [docs](https://api.laposta.nl/doc/index.en.php#fields) |
| [Delete List](actions/delete-list.md) | `DELETE /list/:listId` | [docs](https://api.laposta.nl/doc/index.en.php#lists) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /member/:memberId` | [docs](https://api.laposta.nl/doc/index.en.php#members) |
| [Get Field](actions/get-field.md) | `GET /field/:fieldId` | [docs](https://api.laposta.nl/doc/index.en.php#fields) |
| [Get List](actions/get-list.md) | `GET /list/:listId` | [docs](https://api.laposta.nl/doc/index.en.php#lists) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /member/:memberId` | [docs](https://api.laposta.nl/doc/index.en.php#members) |
| [List Fields](actions/list-fields.md) | `GET /field` | [docs](https://api.laposta.nl/doc/index.en.php#fields) |
| [List Lists](actions/list-lists.md) | `GET /list` | [docs](https://api.laposta.nl/doc/index.en.php#lists) |
| [List Segments](actions/list-segments.md) | `GET /segment` | [docs](https://api.laposta.nl/doc/index.en.php#segments) |
| [List Subscribers](actions/list-subscribers.md) | `GET /member` | [docs](https://api.laposta.nl/doc/index.en.php#members) |
| [Update Field](actions/update-field.md) | `POST /field/:fieldId` | [docs](https://api.laposta.nl/doc/index.en.php#fields) |
| [Update List](actions/update-list.md) | `POST /list/:listId` | [docs](https://api.laposta.nl/doc/index.en.php#lists) |
| [Update Subscriber](actions/update-subscriber.md) | `POST /member/:memberId` | [docs](https://api.laposta.nl/doc/index.en.php#members) |
