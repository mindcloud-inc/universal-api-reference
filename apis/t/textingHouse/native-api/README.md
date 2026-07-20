# TextingHouse: Native API Reference

A consolidated summary of TextingHouse's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.textinghouse.com/en/api-sms-http/api-documentation/
- **OpenAPI specification:** https://api.textinghouse.com/api/http/v1/apidoc/swagger-en.yaml
- **API base URL:** `https://api.textinghouse.com/http/v1`

## Authentication

### Basic Username and Password

Use your TextingHouse API username and password. The provider expects these values in request fields named `user` and `pass`.

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

[Official authentication documentation](https://www.textinghouse.com/en/api-sms-http/api-documentation/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `text/plain` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use plain text.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Credit Balance](actions/get-credit-balance.md) | `POST /do` | [docs](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-conscred) |
| [Get SMS Status By API Message ID](actions/get-sms-status-by-api-message-id.md) | `POST /do` | [docs](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-demstatut) |
| [Get SMS Status By Client Message ID](actions/get-sms-status-by-client-message-id.md) | `POST /do` | [docs](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-demstatut) |
| [Send Commercial SMS](actions/send-commercial-sms.md) | `POST /do` | [docs](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-envoimess) |
| [Send Service SMS](actions/send-service-sms.md) | `POST /do` | [docs](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-envoimess) |
| [Send Test SMS To 999](actions/send-test-sms-to999.md) | `POST /do` | [docs](https://www.textinghouse.com/en/api-sms-http/api-documentation/#doc-smstest) |
