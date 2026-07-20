# PubNub: Native API Reference

A consolidated summary of PubNub's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://www.pubnub.com/docs/admin-api
- **API base URL:** `https://admin-api.pubnub.com/v2`

## Authentication

### Admin API Key

Use a PubNub Service Integration API key to authenticate Admin API requests.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · Your PubNub account ID from the Admin Portal or the 1Password PubNub item.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.pubnub.com/docs/general/portal/service-integrations)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Keysets To Customer](actions/assign-keysets-to-customer.md) | `POST /oem/customers/:customerId/keysets` | [docs](https://www.pubnub.com/docs/admin-api/assign-keysets-to-customer) |
| [Create App](actions/create-app.md) | `POST /apps` | [docs](https://www.pubnub.com/docs/admin-api/create-a-new-app) |
| [Create Business Object](actions/create-business-object.md) | `POST /illuminate/business-objects` | [docs](https://www.pubnub.com/docs/illuminate/illuminate-rest-api) |
| [Create Customer](actions/create-customer.md) | `POST /oem/customers` | [docs](https://www.pubnub.com/docs/admin-api/create-a-new-customer) |
| [Create Keyset](actions/create-keyset.md) | `POST /keysets` | [docs](https://www.pubnub.com/docs/admin-api/create-a-new-keyset) |
| [Delete App](actions/delete-app.md) | `DELETE /apps/:id` | [docs](https://www.pubnub.com/docs/admin-api/delete-an-app) |
| [Delete Keyset](actions/delete-keyset.md) | `DELETE /keysets/:id` | [docs](https://www.pubnub.com/docs/admin-api/delete-a-keyset) |
| [Delete Rotated Secret Key](actions/delete-rotated-secret-key.md) | `DELETE /keysets/:keysetId/secret-keys/:secretKeyPrefix` | [docs](https://www.pubnub.com/docs/admin-api/delete-a-rotated-secret-key) |
| [Get App](actions/get-app.md) | `GET /apps/:id` | [docs](https://www.pubnub.com/docs/admin-api/get-app-by-id) |
| [Get Customer](actions/get-customer.md) | `GET /oem/customers/:customerId` | [docs](https://www.pubnub.com/docs/admin-api/get-customer-by-id) |
| [Get Customer By Keyset](actions/get-customer-by-keyset.md) | `GET /oem/keysets/:keysetId/customer` | [docs](https://www.pubnub.com/docs/admin-api/get-customer-by-keyset) |
| [Get Insights Data](actions/get-insights-data.md) | `GET /insights` | [docs](https://www.pubnub.com/docs/admin-api/get-data) |
| [Get Keyset](actions/get-keyset.md) | `GET /keysets/:id` | [docs](https://www.pubnub.com/docs/admin-api/get-keyset-by-id) |
| [Get Keyset Configuration](actions/get-keyset-configuration.md) | `GET /keysets/:id/config` | [docs](https://www.pubnub.com/docs/admin-api/get-keyset-configuration) |
| [Get Top N Insights Data](actions/get-top-n-insights-data.md) | `GET /insights/top` | [docs](https://www.pubnub.com/docs/admin-api/get-top-n-data) |
| [Get Usage Metrics](actions/get-usage-metrics.md) | `GET /usage-metrics` | [docs](https://www.pubnub.com/docs/admin-api/v2026-02-09/get-metrics) |
| [Issue Customer Access Token](actions/issue-customer-access-token.md) | `POST /oem/access-token` | [docs](https://www.pubnub.com/docs/admin-api/issue-customer-access-token) |
| [List Applications For Customer](actions/list-applications-for-customer.md) | `GET /oem/customers/:customerId/applications` | [docs](https://www.pubnub.com/docs/admin-api/list-applications-for-customer) |
| [List Apps](actions/list-apps.md) | `GET /apps` | [docs](https://www.pubnub.com/docs/admin-api/get-all-apps) |
| [List Business Objects](actions/list-business-objects.md) | `GET /illuminate/business-objects` | [docs](https://www.pubnub.com/docs/illuminate/illuminate-rest-api) |
| [List Customers](actions/list-customers.md) | `GET /oem/customers` | [docs](https://www.pubnub.com/docs/admin-api/list-all-customers) |
| [List Dashboards](actions/list-dashboards.md) | `GET /illuminate/dashboards` | [docs](https://www.pubnub.com/docs/illuminate/illuminate-rest-api) |
| [List Decisions](actions/list-decisions.md) | `GET /illuminate/decisions` | [docs](https://www.pubnub.com/docs/illuminate/illuminate-rest-api) |
| [List Keysets](actions/list-keysets.md) | `GET /keysets` | [docs](https://www.pubnub.com/docs/admin-api/list-keysets) |
| [List Keysets For Customer](actions/list-keysets-for-customer.md) | `GET /oem/customers/:customerId/keysets` | [docs](https://www.pubnub.com/docs/admin-api/list-keysets-for-customer) |
| [List Metrics](actions/list-metrics.md) | `GET /illuminate/metrics` | [docs](https://www.pubnub.com/docs/illuminate/illuminate-rest-api) |
| [List Queries](actions/list-queries.md) | `GET /illuminate/queries` | [docs](https://www.pubnub.com/docs/illuminate/illuminate-rest-api) |
| [List Secret Keys For Keyset](actions/list-secret-keys-for-keyset.md) | `GET /keysets/:keysetId/secret-keys` | [docs](https://www.pubnub.com/docs/admin-api/list-secret-keys-for-a-keyset) |
| [Rotate Secret Key](actions/rotate-secret-key.md) | `POST /keysets/:keysetId/secret-keys` | [docs](https://www.pubnub.com/docs/admin-api/rotate-secret-key) |
| [Update App](actions/update-app.md) | `PATCH /apps/:id` | [docs](https://www.pubnub.com/docs/admin-api/update-an-app) |
| [Update Customer](actions/update-customer.md) | `PUT /oem/customers/:customerId` | [docs](https://www.pubnub.com/docs/admin-api/update-customer) |
| [Update Keyset](actions/update-keyset.md) | `PATCH /keysets/:id` | [docs](https://www.pubnub.com/docs/admin-api/update-keyset-name-and-or-type) |
| [Update Keyset Configuration](actions/update-keyset-configuration.md) | `PATCH /keysets/:id/config` | [docs](https://www.pubnub.com/docs/admin-api/update-keyset-configuration) |
| [Update Secret Key Expiration Time](actions/update-secret-key-expiration-time.md) | `PATCH /keysets/:keysetId/secret-keys/:secretKeyPrefix` | [docs](https://www.pubnub.com/docs/admin-api/update-secret-key-expiration-time) |
