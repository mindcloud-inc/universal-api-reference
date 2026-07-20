# Engage: Native API Reference

A consolidated summary of Engage's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834041-api-overview
- **API base URL:** `https://api.engage.so/v1`

## Authentication

### Basic Auth

Use your Engage public key as the username and private key as the password.

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

[Official authentication documentation](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834041-api-overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `next_cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–30). Use `next_cursor` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Customer to Accounts](actions/add-customer-to-accounts.md) | `POST /users/:uid/accounts` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#add-customer-to-accounts) |
| [Add User to Lists](actions/add-user-to-lists.md) | `POST /users/:uid/lists` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#add-user-to-lists) |
| [Archive List](actions/archive-list.md) | `DELETE /lists/:id` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#archive-a-list) |
| [Archive User](actions/archive-user.md) | `POST /users/:uid/archive` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#archive-a-customer-or-account) |
| [Change Account Role](actions/change-account-role.md) | `PUT /users/:uid/accounts/:aid` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#change-account-role) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#create-a-list) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:uid` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#delete-customer-or-account) |
| [Get List](actions/get-list.md) | `GET /lists/:id` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#get-a-list-by-id) |
| [List Account Members](actions/list-account-members.md) | `GET /users/:uid/members` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#get-account-members) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#get-all-list) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#list-users) |
| [Merge Users](actions/merge-users.md) | `POST /users/merge` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#merge-users) |
| [Queue Batch Request](actions/queue-batch-request.md) | `POST /batch` | [docs](https://docs.engage.so/en-us/a/634d516c3713733fec88a7d4-batch-requests) |
| [Remove Customer from Account](actions/remove-customer-from-account.md) | `DELETE /users/:uid/accounts/:aid` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#remove-customer-from-an-account) |
| [Remove Subscriber from List](actions/remove-subscriber-from-list.md) | `DELETE /lists/:id/subscribers/:uid` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#remove-a-subscriber-from-a-list) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:uid` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#retrieve-a-user) |
| [Send Email](actions/send-email.md) | `POST /send/email` | [docs](https://docs.engage.so/en-us/a/650f5a1ba36d1df032bd73aa-transactional-messaging#send-email) |
| [Send SMS](actions/send-sms.md) | `POST /send/sms` | [docs](https://docs.engage.so/en-us/a/650f5a1ba36d1df032bd73aa-transactional-messaging#send-sms) |
| [Subscribe User to List](actions/subscribe-user-to-list.md) | `POST /lists/:id/subscribers` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#subscribe-user-to-a-list) |
| [Track User Event](actions/track-user-event.md) | `POST /users/:uid/events` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#track-user-event) |
| [Update List](actions/update-list.md) | `PUT /lists/:id` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#update-a-list) |
| [Update Subscriber Status](actions/update-subscriber-status.md) | `PUT /lists/:id/subscribers/:uid` | [docs](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#update-subscriber-status) |
| [Update User Attributes](actions/update-user-attributes.md) | `PUT /users/:uid` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#update-attributes) |
| [Update User Type](actions/update-user-type.md) | `POST /users/:uid/convert` | [docs](https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834042-users#change-user-type) |
