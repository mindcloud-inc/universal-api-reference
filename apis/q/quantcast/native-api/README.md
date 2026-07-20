# Quantcast: Native API Reference

A consolidated summary of Quantcast's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.quantcast.com/docs/graphql-api/
- **API base URL:** `https://developers.quantcast.com`

## Authentication

### OAuth2 Client Credentials

OAuth2 client-credentials authentication for the Quantcast GraphQL API.

### Credentials

- **Client ID:** `clientId` · required · Your Quantcast API Key.
- **Token URL:** `tokenUrl` · required · Quantcast OAuth2 token endpoint.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.tokenUrl}}.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `api_access read_reports`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://developers.quantcast.com/docs/get-started/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Metrics Report](actions/get-account-metrics-report.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [Get Async Attributed Actions Report Download URL](actions/get-async-attributed-actions-report-download-url.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [Get Async Metrics Report Download URL](actions/get-async-metrics-report-download-url.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [Get Available Breakdowns And Metrics](actions/get-available-breakdowns-and-metrics.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Accounts](actions/list-accounts.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Adsets](actions/list-adsets.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Cities](actions/list-cities.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Countries](actions/list-countries.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Creative Assignments](actions/list-creative-assignments.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Creatives](actions/list-creatives.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List ISPs](actions/list-isps.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Key Events](actions/list-key-events.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Members](actions/list-members.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Metro Areas](actions/list-metro-areas.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Organizations](actions/list-organizations.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Postcodes](actions/list-postcodes.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Roles](actions/list-roles.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List States](actions/list-states.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Surveys](actions/list-surveys.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Team Members](actions/list-team-members.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List Teams](actions/list-teams.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [List User Account Assignments](actions/list-user-account-assignments.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [Request Async Attributed Actions Report](actions/request-async-attributed-actions-report.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
| [Request Async Metrics Report](actions/request-async-metrics-report.md) | `GET /api/v2/graphql` | [docs](https://developers.quantcast.com/docs/graphql-api/reference/queries/) |
