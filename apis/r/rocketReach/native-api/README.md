# RocketReach: Native API Reference

A consolidated summary of RocketReach's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.rocketreach.co/reference
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/gldb3mmknn95w
- **API base URL:** `https://api.rocketreach.co/api/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.rocketreach.co/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Lookup People](actions/bulk-lookup-people.md) | `POST /bulkLookup` | [docs](https://docs.rocketreach.co/reference/bulk-person-lookup-person-lookup-api) |
| [Bulk Lookup Universal People](actions/bulk-lookup-universal-people.md) | `POST /universal/person/bulk_lookup` | [docs](https://docs.rocketreach.co/reference/create_universal_person_bulk_lookup) |
| [Check Person Lookup Status](actions/check-person-lookup-status.md) | `GET /person/checkStatus` | [docs](https://docs.rocketreach.co/reference/rocketreach-check-person-lookup-status-people-lookup-api) |
| [Check Universal Person Lookup Status](actions/check-universal-person-lookup-status.md) | `GET /universal/person/check_status` | [docs](https://docs.rocketreach.co/reference/check_universal_person_lookup_status) |
| [Create API Key](actions/create-api-key.md) | `POST /account/key/` | [docs](https://docs.rocketreach.co/reference/rocketreach-api-account-newaccount) |
| [Get Account](actions/get-account.md) | `GET /account/` | [docs](https://docs.rocketreach.co/reference/rocketreach-api-account) |
| [Get Universal Account](actions/get-universal-account.md) | `GET /universal/account/` | [docs](https://docs.rocketreach.co/reference/get_universal_account) |
| [Lookup Company](actions/lookup-company.md) | `GET /company/lookup/` | [docs](https://docs.rocketreach.co/reference/company-lookup-api) |
| [Lookup Person](actions/lookup-person.md) | `GET /person/lookup` | [docs](https://docs.rocketreach.co/reference/people-lookup-api) |
| [Lookup Person And Company](actions/lookup-person-and-company.md) | `GET /profile-company/lookup` | [docs](https://docs.rocketreach.co/reference/create_person_and_company_lookup) |
| [Lookup Universal Company](actions/lookup-universal-company.md) | `GET /universal/company/lookup` | [docs](https://docs.rocketreach.co/reference/create_universal_company_lookup) |
| [Lookup Universal Person](actions/lookup-universal-person.md) | `GET /universal/person/lookup` | [docs](https://docs.rocketreach.co/reference/create_universal_person_lookup) |
| [Search Companies](actions/search-companies.md) | `POST /searchCompany` | [docs](https://docs.rocketreach.co/reference/company-search-api) |
| [Search People](actions/search-people.md) | `POST /person/search` | [docs](https://docs.rocketreach.co/reference/people-search-api) |
| [Search Universal Companies](actions/search-universal-companies.md) | `POST /universal/company/search` | [docs](https://docs.rocketreach.co/reference/create_universal_company_search) |
| [Search Universal People](actions/search-universal-people.md) | `POST /universal/person/search` | [docs](https://docs.rocketreach.co/reference/create_universal_person_search) |
