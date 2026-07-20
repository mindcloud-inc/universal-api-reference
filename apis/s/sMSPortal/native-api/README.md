# SMSPortal: Native API Reference

A consolidated summary of SMSPortal's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.smsportal.com/reference
- **API base URL:** `https://rest.smsportal.com/v3`

## Authentication

### Basic Auth

Authenticate SMSPortal requests with the account Client ID and API Secret via HTTP Basic auth.

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

[Official authentication documentation](https://docs.smsportal.com/docs/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Retrieve Balance](actions/retrieve-balance.md) | `GET /Balance` | [docs](https://docs.smsportal.com/reference/balance_get) |
| [Send Messages](actions/send-messages.md) | `POST /BulkMessages` | [docs](https://docs.smsportal.com/reference/bulkmessages_postv3) |
