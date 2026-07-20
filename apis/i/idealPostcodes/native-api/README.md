# Ideal Postcodes: Native API Reference

A consolidated summary of Ideal Postcodes's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.ideal-postcodes.co.uk/docs/api
- **OpenAPI specification:** https://openapi.ideal-postcodes.co.uk/openapi.yaml
- **API base URL:** `https://api.ideal-postcodes.co.uk/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ideal-postcodes.co.uk/docs/guides/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The current page number is read from `result.page`.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cleanse Address](actions/cleanse-address.md) | `POST /cleanse/addresses` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/address-cleanse) |
| [Email Validation](actions/email-validation.md) | `GET /emails` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/email-validation) |
| [Extract Addresses](actions/extract-addresses.md) | `GET /addresses` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/addresses) |
| [Find Address](actions/find-address.md) | `GET /autocomplete/addresses` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/find-address) |
| [Find Place](actions/find-place.md) | `GET /places` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/find-place) |
| [Lookup Postcode](actions/lookup-postcode.md) | `GET /postcodes/:postcode` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/postcodes) |
| [Phone Number Validation](actions/phone-number-validation.md) | `GET /phone_numbers` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/phone-number-validation) |
| [Resolve Address](actions/resolve-address.md) | `GET /autocomplete/addresses/:address/gbr` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/resolve-address) |
| [Resolve Place](actions/resolve-place.md) | `GET /places/:place` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/resolve-place) |
| [Retrieve Address](actions/retrieve-address.md) | `GET /autocomplete/addresses/:address/usa` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/retrieve-address) |
| [Retrieve by UDPRN](actions/retrieve-by-udprn.md) | `GET /udprn/:udprn` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/udprn) |
| [Retrieve by UMPRN](actions/retrieve-by-umprn.md) | `GET /umprn/:umprn` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/umprn) |
| [Verify Address](actions/verify-address.md) | `POST /verify/addresses` | [docs](https://docs.ideal-postcodes.co.uk/docs/api/address-verify) |
