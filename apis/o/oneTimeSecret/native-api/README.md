# One-Time Secret: Native API Reference

A consolidated summary of One-Time Secret's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.onetimesecret.com/en/rest-api/
- **OpenAPI specification:** https://api.onetimesecret.com/doc/api-v2.json
- **API base URL:** `https://us.onetimesecret.com`

## Authentication

### Username and API Token

HTTP Basic Authentication using your Onetime Secret account login as the username and API token as the password.

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

[Official authentication documentation](https://docs.onetimesecret.com/en/rest-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Burn Receipt Secret](actions/v2-burn-secret.md) | `POST /api/v2/receipt/:identifier/burn` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_receipt_burnsecret) |
| [Conceal Secret](actions/v2-conceal-secret.md) | `POST /api/v2/secret/conceal` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_concealsecret) |
| [Generate Secret](actions/v2-generate-secret.md) | `POST /api/v2/secret/generate` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_generatesecret) |
| [Get Supported Locales](actions/v2-get-supported-locales.md) | `GET /api/v2/supported-locales` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_getsupportedlocales) |
| [Guest Burn Secret](actions/v2-guest-burn-secret.md) | `POST /api/v2/guest/receipt/:identifier/burn` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_burnsecret) |
| [Guest Conceal Secret](actions/v2-guest-conceal-secret.md) | `POST /api/v2/guest/secret/conceal` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_concealsecret) |
| [Guest Generate Secret](actions/v2-guest-generate-secret.md) | `POST /api/v2/guest/secret/generate` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_generatesecret) |
| [Guest Reveal Secret](actions/v2-guest-reveal-secret.md) | `POST /api/v2/guest/secret/:identifier/reveal` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_revealsecret) |
| [Guest Show Receipt](actions/v2-guest-show-receipt.md) | `GET /api/v2/guest/receipt/:identifier` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_showreceipt) |
| [Guest Show Secret](actions/v2-guest-show-secret.md) | `GET /api/v2/guest/secret/:identifier` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_guest_showsecret) |
| [List Receipts](actions/v2-list-receipts.md) | `GET /api/v2/receipt/recent` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_listreceipts) |
| [List Secret Status](actions/v2-list-secret-status.md) | `POST /api/v2/secret/status` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_listsecretstatus) |
| [Private Burn Secret](actions/v2-private-burn-secret.md) | `POST /api/v2/private/:identifier/burn` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_private_burnsecret) |
| [Private List Receipts](actions/v2-private-list-receipts.md) | `GET /api/v2/private/recent` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_private_listreceipts) |
| [Private Show Receipt](actions/v2-private-show-receipt.md) | `GET /api/v2/private/:identifier` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_private_showreceipt) |
| [Private Update Receipt](actions/v2-private-update-receipt.md) | `PATCH /api/v2/private/:identifier` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_private_updatereceipt) |
| [Reveal Secret](actions/v2-reveal-secret.md) | `POST /api/v2/secret/:identifier/reveal` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_secret_revealsecret) |
| [Show Receipt](actions/v2-show-receipt.md) | `GET /api/v2/receipt/:identifier` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_showreceipt) |
| [Show Secret](actions/v2-show-secret.md) | `GET /api/v2/secret/:identifier` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_showsecret) |
| [Show Secret Status](actions/v2-show-secret-status.md) | `GET /api/v2/secret/:identifier/status` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_secret_showsecretstatus) |
| [System Status](actions/v2-system-status.md) | `GET /api/v2/status` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_systemstatus) |
| [System Version](actions/v2-system-version.md) | `GET /api/v2/version` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_systemversion) |
| [Update Receipt](actions/v2-update-receipt.md) | `PATCH /api/v2/receipt/:identifier` | [docs](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_updatereceipt) |
