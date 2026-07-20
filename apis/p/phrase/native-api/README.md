# Phrase: Native API Reference

A consolidated summary of Phrase's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developers.phrase.com/en/api/strings/introduction
- **OpenAPI specification:** https://developers.phrase.com/openapi/phrase-strings.json
- **API base URL:** `https://api.phrase.com/v2`

## Authentication

### Platform token exchange

Use a Phrase Platform access token for Phrase Strings. MindCloud exchanges it for a short-lived JWT before API calls.

### Credentials

- **Platform Access Token:** `clientId` · required · Paste the Phrase Platform access token created for the Phrase Strings service.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://eu.phrase.com/idm/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developers.phrase.com/en/api/platform/oauth/token-endpoint)

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `GET /accounts/{id}` | [docs](https://developers.phrase.com/en/api/strings/accounts/get-a-single-account) |
| [Get Project](actions/get-project.md) | `GET /projects/{id}` | [docs](https://developers.phrase.com/en/api/strings/projects/get-a-single-project) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://developers.phrase.com/en/api/strings/accounts/list-accounts) |
| [List Keys](actions/list-keys.md) | `GET /projects/{project_id}/keys` | [docs](https://developers.phrase.com/en/api/strings/keys/list-keys) |
| [List Locales](actions/list-locales.md) | `GET /projects/{project_id}/locales` | [docs](https://developers.phrase.com/en/api/strings/locales/list-locales) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.phrase.com/en/api/strings/projects/list-projects) |
| [List Translations](actions/list-translations.md) | `GET /projects/{project_id}/translations` | [docs](https://developers.phrase.com/en/api/strings/translations/list-all-translations) |
