# SimpleCirc: Native API Reference

A consolidated summary of SimpleCirc's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://simplecirc.com/docs/api
- **API base URL:** `https://simplecirc.com`

## Authentication

### API Token

Connect SimpleCirc with the API token from Account Settings > API.

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

[Official authentication documentation](https://simplecirc.com/docs/api)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create or Update Address](actions/create-or-update-address.md) | `POST /api/v1.2/subscribers/:account_id/addresses` | [docs](https://simplecirc.com/docs/api) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /api/v1.2/subscribers` | [docs](https://simplecirc.com/docs/api) |
| [Create Subscription](actions/create-subscription.md) | `POST /api/v1.2/subscribers/:account_id/subscriptions` | [docs](https://simplecirc.com/docs/api) |
| [List Subscribers](actions/list-subscribers.md) | `GET /api/v1.2/subscribers` | [docs](https://simplecirc.com/docs/api) |
| [Retrieve Subscriber](actions/retrieve-subscriber.md) | `GET /api/v1.2/subscribers/:account_id` | [docs](https://simplecirc.com/docs/api) |
| [Update Subscriber](actions/update-subscriber.md) | `POST /api/v1.2/subscribers/:account_id` | [docs](https://simplecirc.com/docs/api) |
| [Update Subscription](actions/update-subscription.md) | `POST /api/v1.2/subscribers/:account_id/subscriptions/:publication_id` | [docs](https://simplecirc.com/docs/api) |
