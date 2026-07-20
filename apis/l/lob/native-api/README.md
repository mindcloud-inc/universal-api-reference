# Lob: Native API Reference

A consolidated summary of Lob's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://docs.lob.com
- **API base URL:** `https://api.lob.com/v1`

## Authentication

### API Key (Basic Auth)

Use your Lob API key as the username for HTTP Basic auth and leave the password blank.

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

[Official authentication documentation](https://help.lob.com/account-management/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `next_url`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `after` in the query string as the pagination cursor; numbering starts at 0. Follow the complete next-page URL returned by the API.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete US Addresses](actions/autocomplete-us-addresses.md) | `POST /us_autocompletions` | [docs](https://docs.lob.com/#tag/US-Autocompletions/operation/autocompletion) |
| [Bulk Verify International Addresses](actions/bulk-verify-international-addresses.md) | `POST /bulk/intl_verifications` | [docs](https://docs.lob.com/#tag/Intl-Verifications/operation/bulk_intl_verifications) |
| [Bulk Verify US Addresses](actions/bulk-verify-us-addresses.md) | `POST /bulk/us_verifications` | [docs](https://docs.lob.com/#tag/US-Verifications/operation/bulk_us_verifications) |
| [Cancel Check](actions/cancel-check.md) | `DELETE /checks/:chk_id` | [docs](https://docs.lob.com/#tag/Checks/operation/check_cancel) |
| [Cancel Letter](actions/cancel-letter.md) | `DELETE /letters/:ltr_id` | [docs](https://docs.lob.com/#tag/Letters/operation/letter_cancel) |
| [Cancel Postcard](actions/cancel-postcard.md) | `DELETE /postcards/:psc_id` | [docs](https://docs.lob.com/#tag/Postcards/operation/postcard_delete) |
| [Create Address](actions/create-address.md) | `POST /addresses` | [docs](https://docs.lob.com/#tag/Addresses/operation/address_create) |
| [Create Bank Account](actions/create-bank-account.md) | `POST /bank_accounts` | [docs](https://docs.lob.com/#tag/Bank-Accounts/operation/bank_account_create) |
| [Create Check](actions/create-check.md) | `POST /checks` | [docs](https://docs.lob.com/#tag/Checks/operation/check_create) |
| [Create Letter](actions/create-letter.md) | `POST /letters` | [docs](https://docs.lob.com/#tag/Letters/operation/letter_create) |
| [Create Postcard](actions/create-postcard.md) | `POST /postcards` | [docs](https://docs.lob.com/#tag/Postcards/operation/postcard_create) |
| [Delete Address](actions/delete-address.md) | `DELETE /addresses/:adr_id` | [docs](https://docs.lob.com/#tag/Addresses/operation/address_delete) |
| [Delete Bank Account](actions/delete-bank-account.md) | `DELETE /bank_accounts/:bank_id` | [docs](https://docs.lob.com/#tag/Bank-Accounts/operation/bank_account_delete) |
| [List Addresses](actions/list-addresses.md) | `GET /addresses` | [docs](https://docs.lob.com/#tag/Addresses/operation/addresses_list) |
| [List Bank Accounts](actions/list-bank-accounts.md) | `GET /bank_accounts` | [docs](https://docs.lob.com/#tag/Bank-Accounts/operation/bank_accounts_list) |
| [List Checks](actions/list-checks.md) | `GET /checks` | [docs](https://docs.lob.com/#tag/Checks/operation/checks_list) |
| [List Letters](actions/list-letters.md) | `GET /letters` | [docs](https://docs.lob.com/#tag/Letters/operation/letters_list) |
| [List Postcards](actions/list-postcards.md) | `GET /postcards` | [docs](https://docs.lob.com/#tag/Postcards/operation/postcards_list) |
| [Lookup US ZIP Code](actions/lookup-uszip-code.md) | `POST /us_zip_lookups` | [docs](https://docs.lob.com/#tag/Zip-Lookups/operation/zip_lookup) |
| [Retrieve Address](actions/retrieve-address.md) | `GET /addresses/:adr_id` | [docs](https://docs.lob.com/#tag/Addresses/operation/address_retrieve) |
| [Retrieve Bank Account](actions/retrieve-bank-account.md) | `GET /bank_accounts/:bank_id` | [docs](https://docs.lob.com/#tag/Bank-Accounts/operation/bank_account_retrieve) |
| [Retrieve Check](actions/retrieve-check.md) | `GET /checks/:chk_id` | [docs](https://docs.lob.com/#tag/Checks/operation/check_retrieve) |
| [Retrieve Letter](actions/retrieve-letter.md) | `GET /letters/:ltr_id` | [docs](https://docs.lob.com/#tag/Letters/operation/letter_retrieve) |
| [Retrieve Postcard](actions/retrieve-postcard.md) | `GET /postcards/:psc_id` | [docs](https://docs.lob.com/#tag/Postcards/operation/postcard_retrieve) |
| [Verify Bank Account](actions/verify-bank-account.md) | `POST /bank_accounts/:bank_id/verify` | [docs](https://docs.lob.com/#tag/Bank-Accounts/operation/bank_account_verify) |
| [Verify International Address](actions/verify-international-address.md) | `POST /intl_verifications` | [docs](https://docs.lob.com/#tag/Intl-Verifications/operation/intl_verification) |
| [Verify US Address](actions/verify-us-address.md) | `POST /us_verifications` | [docs](https://docs.lob.com/#tag/US-Verifications/operation/us_verification) |
