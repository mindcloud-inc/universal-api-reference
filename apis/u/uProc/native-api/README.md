# UProc: Native API Reference

A consolidated summary of UProc's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.uproc.io/api/
- **API base URL:** `https://api.uproc.io/api/v2`

## Authentication

### Basic Auth

Use your uProc account email as the username and your uProc API key as the password.

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

[Official authentication documentation](https://docs.uproc.io/api/)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Age Is Adult](actions/check-age-is-adult.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is Between](actions/check-age-is-between.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is Greater](actions/check-age-is-greater.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is Greater or Equal](actions/check-age-is-greater-or-equal.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is in the Forties](actions/check-age-is-in-the-forties.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is in the Twenties](actions/check-age-is-in-the-twenties.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is Lower](actions/check-age-is-lower.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is Lower or Equal](actions/check-age-is-lower-or-equal.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Age Is Retired](actions/check-age-is-retired.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Ages Are Equal](actions/check-ages-are-equal.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check ASIN Exists](actions/check-asin-exists.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check ASIN Is Valid](actions/check-asin-is-valid.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check BIC Is Valid](actions/check-bic-is-valid.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Coordinates Are Valid](actions/check-coordinates-are-valid.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Credit Card Checksum](actions/check-credit-card-checksum.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check ES Bank Account Is Valid](actions/check-es-bank-account-is-valid.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Exact Address Exists](actions/check-exact-address-exists.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check IBAN Is Valid](actions/check-iban-is-valid.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Check Street Number Exists](actions/check-street-number-exists.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Advanced Speech by Text](actions/get-advanced-speech-by-text.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Age by Date](actions/get-age-by-date.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Age Range by Date](actions/get-age-range-by-date.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get ASIN by EAN](actions/get-asin-by-ean.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Coordinates by Search](actions/get-coordinates-by-search.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Credit Card Type by Number](actions/get-credit-card-type-by-number.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Exact Address by Search](actions/get-exact-address-by-search.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get IBAN by Account](actions/get-iban-by-account.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get IBAN Lookup](actions/get-iban-lookup.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Normalized Address](actions/get-normalized-address.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Parsed Address](actions/get-parsed-address.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
| [Get Speech by Text](actions/get-speech-by-text.md) | `POST /process` | [docs](https://docs.uproc.io/api/) |
