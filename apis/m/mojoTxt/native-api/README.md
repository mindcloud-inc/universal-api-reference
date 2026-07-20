# MojoTxt: Native API Reference

A consolidated summary of MojoTxt's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://app.mojotxt.com/api/docs/v1/
- **API base URL:** `https://app.mojotxt.com/api/v1`

## Authentication

### Basic

Use your MojoTxt API Username and API Password for HTTP basic authentication.

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

[Official authentication documentation](https://app.mojotxt.com/api/docs/v1/)

## API conventions

Responses from this API use JSON. Response data is read from `records`.

## Pagination

Use `Limit` in the query string to set the page size. Use `Page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `Sort` in the query string. Set the direction separately with `SortDirection`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Donation Keyword](actions/create-donation-keyword.md) | `POST /:phoneNumber/donations/add` | [docs](https://app.mojotxt.com/api/docs/v1/donations-add.php) |
| [Create Message](actions/create-message.md) | `POST /:phoneNumber/messages/add` | [docs](https://app.mojotxt.com/api/docs/v1/messages-add.php) |
| [Create Subscription List](actions/create-subscription-list.md) | `POST /:phoneNumber/lists/add` | [docs](https://app.mojotxt.com/api/docs/v1/lists-add.php) |
| [Delete Donation](actions/delete-donation.md) | `POST /:phoneNumber/donations/delete/:donationIdOrKeyword` | [docs](https://app.mojotxt.com/api/docs/v1/donations-delete.php) |
| [Delete Message](actions/delete-message.md) | `POST /:phoneNumber/messages/delete/:messageId` | [docs](https://app.mojotxt.com/api/docs/v1/messages-delete.php) |
| [Delete Subscription List](actions/delete-subscription-list.md) | `POST /:phoneNumber/lists/delete/:listIdOrKeyword` | [docs](https://app.mojotxt.com/api/docs/v1/lists-delete.php) |
| [Export Donations](actions/export-donations.md) | `GET /:phoneNumber/donations/export/:donationIdOrKeyword` | [docs](https://app.mojotxt.com/api/docs/v1/donations-export.php) |
| [Get Donation](actions/get-donation.md) | `GET /:phoneNumber/donations/get/:donationIdOrKeyword` | [docs](https://app.mojotxt.com/api/docs/v1/donations-get.php) |
| [Get Message](actions/get-message.md) | `GET /:phoneNumber/messages/get/:messageId` | [docs](https://app.mojotxt.com/api/docs/v1/messages-get.php) |
| [Get Subscription List](actions/get-subscription-list.md) | `GET /:phoneNumber/lists/get/:listIdOrKeyword` | [docs](https://app.mojotxt.com/api/docs/v1/lists-get.php) |
| [List Donations](actions/list-donations.md) | `GET /:phoneNumber/donations/list` | [docs](https://app.mojotxt.com/api/docs/v1/donations-list.php) |
| [List Message Log](actions/list-message-log.md) | `GET /:phoneNumber/messageLog/list` | [docs](https://app.mojotxt.com/api/docs/v1/messagelog.php#list) |
| [List Messages](actions/list-messages.md) | `GET /:phoneNumber/messages/list` | [docs](https://app.mojotxt.com/api/docs/v1/messages-list.php) |
| [List Phone Number Subscribers](actions/list-phone-number-subscribers.md) | `GET /:phoneNumber/subscribers/list` | [docs](https://app.mojotxt.com/api/docs/v1/subscribers-list.php) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /phoneNumbers/list` | [docs](https://app.mojotxt.com/api/docs/v1/phoneNumbers-list.php) |
| [List Subscribers](actions/list-subscribers.md) | `GET /subscribers/list` | [docs](https://app.mojotxt.com/api/docs/v1/subscribers-list.php) |
| [List Subscription Lists](actions/list-subscription-lists.md) | `GET /:phoneNumber/lists/list` | [docs](https://app.mojotxt.com/api/docs/v1/lists-list.php) |
| [Update Donation Keyword](actions/update-donation-keyword.md) | `POST /:phoneNumber/donations/update/:donationIdOrKeyword` | [docs](https://app.mojotxt.com/api/docs/v1/donations-update.php) |
| [Update Message](actions/update-message.md) | `POST /:phoneNumber/messages/update/:messageId` | [docs](https://app.mojotxt.com/api/docs/v1/messages-update.php) |
| [Update Subscription List](actions/update-subscription-list.md) | `POST /:phoneNumber/lists/update/:listIdOrKeyword` | [docs](https://app.mojotxt.com/api/docs/v1/lists-update.php) |
