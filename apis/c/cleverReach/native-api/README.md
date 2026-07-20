# CleverReach: Native API Reference

A consolidated summary of CleverReach's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://rest.cleverreach.com/explorer/v3/
- **OpenAPI specification:** https://rest.cleverreach.com/v3/resources.json
- **API base URL:** `https://rest.cleverreach.com`

## Authentication

### OAuth2

Create the OAuth app in CleverReach under Account > Interfaces > REST API, register the MindCloud callback URL, then connect the account.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://rest.cleverreach.com/oauth/authorize.php to approve access.
2. Exchange the returned authorization code with a POST request to https://rest.cleverreach.com/oauth/token.php.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://rest.cleverreach.com/oauth/token.php. A machine-to-machine flow is configured.

[Official authentication documentation](https://rest.cleverreach.com/howto/index.php#oauth)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Group Filter Receivers](actions/count-group-filter-receivers.md) | `GET /v3/groups.json/:groupId/filters/:filterId/count` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [Get Attribute Limits](actions/get-attribute-limits.md) | `GET /v3/attributes/limits.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/attributes-v3.json) |
| [Get Blacklist Entry](actions/get-blacklist-entry.md) | `GET /v3/blacklist.json/:email` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/blacklist-v3.json) |
| [Get Form](actions/get-form.md) | `GET /v3/forms.json/:id` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/forms-v3.json) |
| [Get Form Embedded Code](actions/get-form-embedded-code.md) | `GET /v3/forms.json/:id/code` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/forms-v3.json) |
| [Get Group](actions/get-group.md) | `GET /v3/groups.json/:id` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [Get Group Filter](actions/get-group-filter.md) | `GET /v3/groups.json/:groupId/filters/:filterId` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [Get Group Filter Stats](actions/get-group-filter-stats.md) | `GET /v3/groups.json/:groupId/filters/:filterId/stats` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [Get Group Receiver](actions/get-group-receiver.md) | `GET /v3/groups.json/:groupId/receivers/:poolId` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [Get Group Stats](actions/get-group-stats.md) | `GET /v3/groups.json/:id/stats` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [Get Mailing](actions/get-mailing.md) | `GET /v3/mailings.json/:id` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/mailings-v3.json) |
| [Get Receiver](actions/get-receiver.md) | `GET /v3/receivers.json/:id` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/receivers-v3.json) |
| [Get Report](actions/get-report.md) | `GET /v3/reports.json/:id` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/reports-v3.json) |
| [Get Report Stats](actions/get-report-stats.md) | `GET /v3/reports.json/:id/stats/:mode` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/reports-v3.json) |
| [List Attributes](actions/list-attributes.md) | `GET /v3/attributes.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/attributes-v3.json) |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | `GET /v3/blacklist.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/blacklist-v3.json) |
| [List Bounces](actions/list-bounces.md) | `GET /v3/bounces.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/bounces-v3.json) |
| [List Forms](actions/list-forms.md) | `GET /v3/forms.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/forms-v3.json) |
| [List Group Attributes](actions/list-group-attributes.md) | `GET /v3/groups.json/:groupId/attributes` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [List Group Filter Receivers](actions/list-group-filter-receivers.md) | `GET /v3/groups.json/:groupId/filters/:filterId/receivers` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [List Group Filters](actions/list-group-filters.md) | `GET /v3/groups.json/:groupId/filters` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [List Group Forms](actions/list-group-forms.md) | `GET /v3/groups.json/:id/forms` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [List Group Receiver Events](actions/list-group-receiver-events.md) | `GET /v3/groups.json/:groupId/receivers/:poolId/events` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [List Group Receivers](actions/list-group-receivers.md) | `GET /v3/groups.json/:groupId/receivers` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [List Groups](actions/list-groups.md) | `GET /v3/groups.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/groups-v3.json) |
| [List Mailing Links](actions/list-mailing-links.md) | `GET /v3/mailings.json/:id/links` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/mailings-v3.json) |
| [List Mailings](actions/list-mailings.md) | `GET /v3/mailings.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/mailings-v3.json) |
| [List Receiver Groups](actions/list-receiver-groups.md) | `GET /v3/receivers.json/:id/groups` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/receivers-v3.json) |
| [List Report Receivers by State](actions/list-report-receivers-by-state.md) | `GET /v3/reports.json/:id/receivers/:state` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/reports-v3.json) |
| [List Reports](actions/list-reports.md) | `GET /v3/reports.json` | [docs](https://rest.cleverreach.com/explorer/v3/?url=https://rest.cleverreach.com/v3/resources/reports-v3.json) |
