# Favro: Native API Reference

A consolidated summary of Favro's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://favro.com/developer/
- **API base URL:** `https://favro.com/api/v1`

## Authentication

### Basic Auth

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

[Official authentication documentation](https://favro.com/developer/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | `POST /cards` | [docs](https://favro.com/developer/) |
| [Create Collection](actions/create-collection.md) | `POST /collections` | [docs](https://favro.com/developer/) |
| [Create Widget](actions/create-widget.md) | `POST /widgets` | [docs](https://favro.com/developer/) |
| [Delete Card](actions/delete-card.md) | `DELETE /cards/:cardId` | [docs](https://favro.com/developer/) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /collections/:collectionId` | [docs](https://favro.com/developer/) |
| [Delete Widget](actions/delete-widget.md) | `DELETE /widgets/:widgetCommonId` | [docs](https://favro.com/developer/) |
| [Get All Cards](actions/get-all-cards.md) | `GET /cards` | [docs](https://favro.com/developer/) |
| [Get All Collections](actions/get-all-collections.md) | `GET /collections` | [docs](https://favro.com/developer/) |
| [Get All Columns](actions/get-all-columns.md) | `GET /columns` | [docs](https://favro.com/developer/) |
| [Get All Users](actions/get-all-users.md) | `GET /users` | [docs](https://favro.com/developer/) |
| [Get All Widgets](actions/get-all-widgets.md) | `GET /widgets` | [docs](https://favro.com/developer/) |
| [Get Card](actions/get-card.md) | `GET /cards/:cardId` | [docs](https://favro.com/developer/) |
| [Get Collection](actions/get-collection.md) | `GET /collections/:collectionId` | [docs](https://favro.com/developer/) |
| [Get Column](actions/get-column.md) | `GET /columns/:columnId` | [docs](https://favro.com/developer/) |
| [Get Organizations](actions/get-organizations.md) | `GET /organizations` | [docs](https://favro.com/developer/) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://favro.com/developer/) |
| [Get Widget](actions/get-widget.md) | `GET /widgets/:widgetCommonId` | [docs](https://favro.com/developer/) |
| [Update Card](actions/update-card.md) | `PUT /cards/:cardId` | [docs](https://favro.com/developer/) |
| [Update Collection](actions/update-collection.md) | `PUT /collections/:collectionId` | [docs](https://favro.com/developer/) |
| [Update Widget](actions/update-widget.md) | `PUT /widgets/:widgetCommonId` | [docs](https://favro.com/developer/) |
