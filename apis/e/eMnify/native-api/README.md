# EMnify: Native API Reference

A consolidated summary of EMnify's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.emnify.com/developers
- **API base URL:** `https://cdn.emnify.net/api/v1`

## Authentication

### Application Token

Authenticate EMnify REST API access with an application token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.emnify.com/developers/auth/application-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (maximum 2500). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Use `+` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Application Token](actions/create-application-token.md) | `POST /application_token` | [docs](https://docs.emnify.com/developers/api/application-tokens/application-token-post) |
| [Create Endpoint](actions/create-endpoint.md) | `POST /endpoint` | [docs](https://docs.emnify.com/developers/api/endpoint/create-endpoint) |
| [Create Service Profile](actions/create-service-profile.md) | `POST /service_profile` | [docs](https://docs.emnify.com/developers/api/service-profiles/service-profile-post) |
| [Delete Endpoint](actions/delete-endpoint.md) | `DELETE /endpoint/:endpoint_id` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-by-id-delete) |
| [Get Endpoint Details](actions/get-endpoint-details.md) | `GET /endpoint/:endpoint_id` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-by-id-get) |
| [Get Endpoint Usage And Cost Statistics](actions/get-endpoint-usage-and-cost-statistics.md) | `GET /endpoint/:endpoint_id/stats` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-stats-by-id-get) |
| [Get Monthly Organization Traffic And Cost Statistics](actions/get-monthly-organization-traffic-and-cost-statistics.md) | `GET /organisation/:org_id_or_my/stats` | [docs](https://docs.emnify.com/developers/api/organization/get-organisation-monthly-stats) |
| [Get My Organization Details](actions/get-my-organization-details.md) | `GET /organisation/my` | [docs](https://docs.emnify.com/developers/api/organization/my-organisation-get) |
| [Get Tariff Profile Details](actions/get-tariff-profile-details.md) | `GET /tariff_profile/:tariff_profile_id` | [docs](https://docs.emnify.com/developers/api/tariff-profiles/tariff-profile-by-id-get) |
| [List Application Tokens](actions/list-application-tokens.md) | `GET /application_token` | [docs](https://docs.emnify.com/developers/api/application-tokens/application-token-get) |
| [List Endpoint Events](actions/list-endpoint-events.md) | `GET /endpoint/:endpoint_id/event` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-events-by-id) |
| [List Endpoint SMS Messages](actions/list-endpoint-sms-messages.md) | `GET /endpoint/:endpoint_id/sms` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-sms-by-id-get) |
| [List Endpoint Statuses](actions/list-endpoint-statuses.md) | `GET /endpoint/status` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-status-get) |
| [List Endpoints](actions/list-endpoints.md) | `GET /endpoint` | [docs](https://docs.emnify.com/developers/api/endpoint/get-endpoints) |
| [List Event Types](actions/list-event-types.md) | `GET /event/type` | [docs](https://docs.emnify.com/developers/api/events/event-type-get) |
| [List Events](actions/list-events.md) | `GET /event` | [docs](https://docs.emnify.com/developers/api/events/get-events) |
| [List Service Profiles](actions/list-service-profiles.md) | `GET /service_profile` | [docs](https://docs.emnify.com/developers/api/service-profiles/service-profile-get) |
| [List SIM Statuses](actions/list-sim-statuses.md) | `GET /sim/status` | [docs](https://docs.emnify.com/developers/api/sim/sim-status-get) |
| [List SIMs](actions/list-sims.md) | `GET /sim` | [docs](https://docs.emnify.com/developers/api/sim/sim-per-page-sort-by-q-and-page-get) |
| [List Tariff Profiles](actions/list-tariff-profiles.md) | `GET /tariff_profile` | [docs](https://docs.emnify.com/developers/api/tariff-profiles/tariff-profile-get) |
| [Retrieve Authentication Token](actions/retrieve-authentication-token.md) | `POST /authenticate` | [docs](https://docs.emnify.com/developers/api/authentication/authenticate) |
| [Retrieve Endpoint Connectivity Information](actions/retrieve-endpoint-connectivity-information.md) | `GET /endpoint/:endpoint_id/connectivity_info` | [docs](https://docs.emnify.com/developers/api/endpoint/get-connectivity-info-by-endpoint-id) |
| [Retrieve Endpoint Data Quota Details](actions/retrieve-endpoint-data-quota-details.md) | `GET /endpoint/:endpoint_id/quota/data` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-quota-data-by-endpoint-id-get) |
| [Retrieve Service Profile](actions/retrieve-service-profile.md) | `GET /service_profile/:profile_id` | [docs](https://docs.emnify.com/developers/api/service-profiles/service-profile-by-profile-id-get) |
| [Set Endpoint Data Quota](actions/set-endpoint-data-quota.md) | `POST /endpoint/:endpoint_id/quota/data` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-quota-data-by-endpoint-id-post) |
| [Update Application Token](actions/update-application-token.md) | `PATCH /application_token/:application_token_id` | [docs](https://docs.emnify.com/developers/api/application-tokens/application-token-by-id-patch) |
| [Update Endpoint](actions/update-endpoint.md) | `PATCH /endpoint/:endpoint_id` | [docs](https://docs.emnify.com/developers/api/endpoint/endpoint-by-id-patch) |
| [Update Service Profile](actions/update-service-profile.md) | `PATCH /service_profile/:profile_id` | [docs](https://docs.emnify.com/developers/api/service-profiles/service-profile-by-profile-id-patch) |
