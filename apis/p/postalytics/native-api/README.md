# Postalytics: Native API Reference

A consolidated summary of Postalytics's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://docs.postalytics.com/references/postalytics-rest-api
- **API base URL:** `https://api.postalytics.com`

## Authentication

### Basic

Authenticate with your Postalytics API key as the Basic-auth username and leave the password blank.

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

[Official authentication documentation](https://docs.postalytics.com/getting-started/authentication-0)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Suppression List](actions/create-suppression-list.md) | `POST /api/v1/lists/suppression` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/create-suppression-list) |
| [Create Suppression List Contact](actions/create-suppression-list-contact.md) | `POST /api/v1/lists/suppression/contacts/:listId` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/create-suppression-list-contact) |
| [Delete Suppression List](actions/delete-suppression-list.md) | `DELETE /api/v1/lists/suppression/:id` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/delete-suppression-list) |
| [Delete Suppression List Contact](actions/delete-suppression-list-contact.md) | `DELETE /api/v1/lists/suppression/contacts/:listId/:contactId` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/delete-suppression-list-contact) |
| [Get My Account](actions/get-my-account.md) | `GET /api/v1/account/me` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/get-my-account) |
| [Get Suppression List](actions/get-suppression-list.md) | `GET /api/v1/lists/suppression/:id` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/get-suppression-list) |
| [Get Suppression List Contact](actions/get-suppression-list-contact.md) | `GET /api/v1/lists/suppression/contacts/:listId/:contactId` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/get-suppression-list-contact) |
| [List Suppression List Contacts](actions/list-suppression-list-contacts.md) | `GET /api/v1/lists/suppression/contacts/:listId` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/get-suppression-list-contacts) |
| [List Suppression Lists](actions/list-suppression-lists.md) | `GET /api/v1/lists/suppression` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/get-suppression-lists) |
| [Update Suppression List Contact](actions/update-suppression-list-contact.md) | `PUT /api/v1/lists/suppression/contacts/:listId/:contactId` | [docs](https://docs.postalytics.com/references/postalytics-rest-api/update-suppression-list-contact) |
