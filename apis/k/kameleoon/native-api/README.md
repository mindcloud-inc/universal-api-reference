# Kameleoon: Native API Reference

A consolidated summary of Kameleoon's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developers.kameleoon.com/apis/automation-api-rest/get-started/
- **API base URL:** `https://api.kameleoon.com`

## Authentication

### OAuth 2.0

Use Kameleoon OAuth2 client credentials for server-to-server API access. Authorization-code flow is available for partner distribution use cases.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.kameleoon.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.kameleoon.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developers.kameleoon.com/apis/automation-api-rest/api-reference/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create account](actions/create-account.md) | `POST accounts` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/create-account/) |
| [Delete account](actions/delete-account.md) | `DELETE accounts/:accountId` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/delete-account/) |
| [Get account](actions/get-account.md) | `GET accounts/:accountId` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-account/) |
| [Get all accounts](actions/get-all-accounts.md) | `GET accounts` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-accounts/) |
| [Get all custom data](actions/get-all-custom-data.md) | `GET custom-datas` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-custom-data/) |
| [Get all experiments](actions/get-all-experiments.md) | `GET experiments` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-experiments/) |
| [Get all goals](actions/get-all-goals.md) | `GET goals` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-goals/) |
| [Get all images](actions/get-all-images.md) | `GET images` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-images/) |
| [Get all key moments](actions/get-all-key-moments.md) | `GET key-moments` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-key-moments/) |
| [Get all key pages](actions/get-all-key-pages.md) | `GET key-pages` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-key-pages/) |
| [Get all personalizations](actions/get-all-personalizations.md) | `GET personalizations` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-personalizations/) |
| [Get all referrers](actions/get-all-referrers.md) | `GET referrers` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-referrers/) |
| [Get all segments](actions/get-all-segments.md) | `GET segments` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-segments/) |
| [Get all sites](actions/get-all-sites.md) | `GET sites` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-sites/) |
| [Get all studio recommender blocks](actions/get-all-studio-recommender-blocks.md) | `GET studio-recommender-blocks` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-studio-recommender-blocks/) |
| [Get all tags](actions/get-all-tags.md) | `GET tags` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-tags/) |
| [Get all targeting rules](actions/get-all-targeting-rules.md) | `GET targeting-rules` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-targeting-rules/) |
| [Get all variations](actions/get-all-variations.md) | `GET variations` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-variations/) |
| [Get all widget studio templates](actions/get-all-widget-studio-templates.md) | `GET widget-studio-templates` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-widget-studio-templates/) |
| [Get all widget studios](actions/get-all-widget-studios.md) | `GET widget-studio` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-widget-studios/) |
| [Get all widget templates](actions/get-all-widget-templates.md) | `GET templates` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/get-all-widget-templates/) |
| [Update account](actions/update-account.md) | `PATCH accounts/:accountId` | [docs](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/partial-update-account/) |
