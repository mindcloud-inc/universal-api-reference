# RECRU: Native API Reference

A consolidated summary of RECRU's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://mindclo.recru.eu/api/index/documentation
- **API base URL:** `https://mindclo.recru.eu/api/json-rpc`

## Authentication

### Login (Email + Password)

Authenticates with RECRU using login and password via AuthService.login, then reuses the returned bearer token.

### Credentials

- **Login:** `login` · required · RECRU login for the API user.
- **Password:** `password` · required · RECRU main password for the API user.

Send these headers with each API request:

```http
Authorization: Bearer <custom.token>
```

[Official authentication documentation](https://mindclo.recru.eu/api/index/documentation#AuthService_login)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Newsletter Unsubscribe](actions/add-newsletter-unsubscribe.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Echo Text](actions/echo-text.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Allowed Mobile App Menu Items](actions/get-allowed-mobile-app-menu-items.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Client Save Metadata](actions/get-client-save-metadata.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Colors](actions/get-colors.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Country Pairs](actions/get-country-pairs.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Event Types](actions/get-event-types.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Jobseeker Apply Metadata](actions/get-jobseeker-apply-metadata.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Jobseeker Save Metadata](actions/get-jobseeker-save-metadata.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Jobseeker Sources](actions/get-jobseeker-sources.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Locales](actions/get-locales.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Multiple Codebooks](actions/get-multiple-codebooks.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Project Close Reasons](actions/get-project-close-reasons.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Project Save Metadata](actions/get-project-save-metadata.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get Rejection Reasons](actions/get-rejection-reasons.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get SK NACE Pairs](actions/get-sk-nace-pairs.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Get User Name Pairs](actions/get-user-name-pairs.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Login](actions/login.md) | `POST` |  |
| [Ping](actions/ping.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Remove Newsletter Unsubscribe](actions/remove-newsletter-unsubscribe.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
| [Set Viewed Tour](actions/set-viewed-tour.md) | `POST` | [docs](https://mindclo.recru.eu/api/index/documentation) |
