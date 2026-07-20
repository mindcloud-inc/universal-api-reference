# ServiceTrade: Native API Reference

A consolidated summary of ServiceTrade's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.servicetrade.com/api/docs
- **API base URL:** `https://api.servicetrade.com/api`

## Authentication

### OAuth2 Client Credentials

Legacy OAuth2 client-credentials auth retained only for internal migration fallback; end users should connect with ServiceTrade username and password instead.

### Credentials

- **Client Secret:** `clientSecret` · required · The ServiceTrade OAuth2 client_secret value for your tenant.
- **Client ID:** `clientId` · required · The ServiceTrade OAuth2 client_id value for your tenant.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.servicetrade.com/api/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.servicetrade.com/api/oauth2/token. A machine-to-machine flow is configured.

[Official authentication documentation](https://api.servicetrade.com/api/docs#resource-oauth2credentials)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The total page count is read from `data.totalPages`. The current page number is read from `data.page`.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | `POST asset` | [docs](https://api.servicetrade.com/api/docs#resource-asset) |
| [Create Job](actions/create-job.md) | `POST job` | [docs](https://api.servicetrade.com/api/docs#resource-job) |
| [Create Location](actions/create-location.md) | `POST location` | [docs](https://api.servicetrade.com/api/docs#resource-location) |
| [Create Quote](actions/create-quote.md) | `POST quote` | [docs](https://api.servicetrade.com/api/docs#resource-quote) |
| [Create Service Request](actions/create-service-request.md) | `POST servicerequest` | [docs](https://api.servicetrade.com/api/docs#resource-servicerequest) |
| [Get Asset by ID](actions/get-asset-by-id.md) | `GET asset/:assetId` | [docs](https://api.servicetrade.com/api/docs#resource-asset) |
| [Get Company by ID](actions/get-company-by-id.md) | `GET company/:companyId` | [docs](https://api.servicetrade.com/api/docs#resource-company) |
| [Get Contact by ID](actions/get-contact-by-id.md) | `GET contact/:contactId` | [docs](https://api.servicetrade.com/api/docs#resource-contact) |
| [Get Job by ID](actions/get-job-by-id.md) | `GET job/:jobId` | [docs](https://api.servicetrade.com/api/docs#resource-job) |
| [Get Location by ID](actions/get-location-by-id.md) | `GET location/:locationId` | [docs](https://api.servicetrade.com/api/docs#resource-location) |
| [Get OAuth2 Userinfo](actions/get-oauth2-userinfo.md) | `GET oauth2/userinfo` | [docs](https://api.servicetrade.com/api/docs#resource-oauth2userinfo) |
| [Get Quote by ID](actions/get-quote-by-id.md) | `GET quote/:quoteId` | [docs](https://api.servicetrade.com/api/docs#resource-quote) |
| [Get Service Request by ID](actions/get-service-request-by-id.md) | `GET servicerequest/:serviceRequestId` | [docs](https://api.servicetrade.com/api/docs#resource-servicerequest) |
| [List Assets](actions/list-assets.md) | `GET asset` | [docs](https://api.servicetrade.com/api/docs#resource-asset) |
| [List Companies](actions/list-companies.md) | `GET company` | [docs](https://api.servicetrade.com/api/docs#resource-company) |
| [List Contacts](actions/list-contacts.md) | `GET contact` | [docs](https://api.servicetrade.com/api/docs#resource-contact) |
| [List Jobs](actions/list-jobs.md) | `GET job` | [docs](https://api.servicetrade.com/api/docs#resource-job) |
| [List Locations](actions/list-locations.md) | `GET location` | [docs](https://api.servicetrade.com/api/docs#resource-location) |
| [List Quotes](actions/list-quotes.md) | `GET quote` | [docs](https://api.servicetrade.com/api/docs#resource-quote) |
| [List Service Requests](actions/list-service-requests.md) | `GET servicerequest` | [docs](https://api.servicetrade.com/api/docs#resource-servicerequest) |
| [Update Asset](actions/update-asset.md) | `PUT asset/:assetId` | [docs](https://api.servicetrade.com/api/docs#resource-asset) |
| [Update Job](actions/update-job.md) | `PUT job/:jobId` | [docs](https://api.servicetrade.com/api/docs#resource-job) |
| [Update Location](actions/update-location.md) | `PUT location/:locationId` | [docs](https://api.servicetrade.com/api/docs#resource-location) |
| [Update Quote](actions/update-quote.md) | `PUT quote/:quoteId` | [docs](https://api.servicetrade.com/api/docs#resource-quote) |
| [Update Service Request](actions/update-service-request.md) | `PUT servicerequest/:serviceRequestId` | [docs](https://api.servicetrade.com/api/docs#resource-servicerequest) |
