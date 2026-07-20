# Control D: Native API Reference

A consolidated summary of Control D's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.controld.com/reference
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/h3s35mmmtqlto
- **API base URL:** `https://api.controld.com`

## Authentication

### API Key

Use a Control D API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.controld.com/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `body`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Modify Filters](actions/batch-modify-filters.md) | `PUT /profiles/:profileId/filters` | [docs](https://docs.controld.com/reference/put_profiles-profile-id-filters) |
| [Create Custom Rule](actions/create-custom-rule.md) | `POST /profiles/:profileId/rules` | [docs](https://docs.controld.com/reference/post_profiles-profile-id-rules) |
| [Create Endpoint](actions/create-endpoint.md) | `POST /devices` | [docs](https://docs.controld.com/reference/post_devices) |
| [Create Profile](actions/create-profile.md) | `POST /profiles` | [docs](https://docs.controld.com/reference/post_profiles) |
| [Create Rule Folder](actions/create-rule-folder.md) | `POST /profiles/:profileId/groups` | [docs](https://docs.controld.com/reference/post_profiles-profile-id-groups) |
| [Create Sub-Organization](actions/create-sub-organization.md) | `POST /organizations/suborg` | [docs](https://docs.controld.com/reference/post_organizations-suborg) |
| [Get Current IP](actions/get-current-ip.md) | `GET /ip` | [docs](https://docs.controld.com/reference/get_ip) |
| [Get Default Rule](actions/get-default-rule.md) | `GET /profiles/:profileId/default` | [docs](https://docs.controld.com/reference/get_profiles-profile-id-default) |
| [Get Network Stats](actions/get-network-stats.md) | `GET /network` | [docs](https://docs.controld.com/reference/get_network) |
| [Get Organization Info](actions/get-organization-info.md) | `GET /organizations/organization` | [docs](https://docs.controld.com/reference/get_organizations-organization) |
| [Get User Data](actions/get-user-data.md) | `GET /users` | [docs](https://docs.controld.com/reference/get_users) |
| [Learn New IP](actions/learn-new-ip.md) | `POST /access` | [docs](https://docs.controld.com/reference/post_access) |
| [List Active Products](actions/list-active-products.md) | `GET /billing/products` | [docs](https://docs.controld.com/reference/get_billing-products) |
| [List Custom Rules](actions/list-custom-rules.md) | `GET /profiles/:profileId/rules/:folderId` | [docs](https://docs.controld.com/reference/get_profiles-profile-id-rules-folder-id) |
| [List Endpoint Types](actions/list-endpoint-types.md) | `GET /devices/types` | [docs](https://docs.controld.com/reference/get_devices-types) |
| [List Endpoints](actions/list-endpoints.md) | `GET /devices` | [docs](https://docs.controld.com/reference/get_devices) |
| [List External Filters](actions/list-external-filters.md) | `GET /profiles/:profileId/filters/external` | [docs](https://docs.controld.com/reference/get_profiles-profile-id-filters-external) |
| [List Known IPs](actions/list-known-ips.md) | `GET /access` | [docs](https://docs.controld.com/reference/get_access) |
| [List Log Levels](actions/list-log-levels.md) | `GET /analytics/levels` | [docs](https://docs.controld.com/reference/get_analytics-levels) |
| [List Native Filters](actions/list-native-filters.md) | `GET /profiles/:profileId/filters` | [docs](https://docs.controld.com/reference/get_profiles-profile-id-filters) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organizations/members` | [docs](https://docs.controld.com/reference/get_organizations-members) |
| [List Payments](actions/list-payments.md) | `GET /billing/payments` | [docs](https://docs.controld.com/reference/get_billing-payments) |
| [List Profile Options](actions/list-profile-options.md) | `GET /profiles/options` | [docs](https://docs.controld.com/reference/get_profiles-options) |
| [List Profile Services](actions/list-profile-services.md) | `GET /profiles/:profileId/services` | [docs](https://docs.controld.com/reference/get_profiles-profile-id-services) |
| [List Profiles](actions/list-profiles.md) | `GET /profiles` | [docs](https://docs.controld.com/reference/get_profiles) |
| [List Proxies](actions/list-proxies.md) | `GET /proxies` | [docs](https://docs.controld.com/reference/get_proxies) |
| [List Rule Folders](actions/list-rule-folders.md) | `GET /profiles/:profileId/groups` | [docs](https://docs.controld.com/reference/get_profiles-profile-id-groups) |
| [List Service Categories](actions/list-service-categories.md) | `GET /services/categories` | [docs](https://docs.controld.com/reference/get_services-categories) |
| [List Services In Category](actions/list-services-in-category.md) | `GET /services/categories/:category` | [docs](https://docs.controld.com/reference/get_services-categories-category) |
| [List Storage Regions](actions/list-storage-regions.md) | `GET /analytics/endpoints` | [docs](https://docs.controld.com/reference/get_analytics-endpoints) |
| [List Sub-Organizations](actions/list-sub-organizations.md) | `GET /organizations/sub_organizations` | [docs](https://docs.controld.com/reference/get_organizations-sub_organizations) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /billing/subscriptions` | [docs](https://docs.controld.com/reference/get_billing-subscriptions) |
| [Modify Custom Rule](actions/modify-custom-rule.md) | `PUT /profiles/:profileId/rules` | [docs](https://docs.controld.com/reference/put_profiles-profile-id-rules) |
| [Modify Default Rule](actions/modify-default-rule.md) | `PUT /profiles/:profileId/default` | [docs](https://docs.controld.com/reference/put_profiles-profile-id-default) |
| [Modify Endpoint](actions/modify-endpoint.md) | `PUT /devices/:deviceId` | [docs](https://docs.controld.com/reference/put_devices-device-id) |
| [Modify Filter](actions/modify-filter.md) | `PUT /profiles/:profileId/filters/filter/:filter` | [docs](https://docs.controld.com/reference/put_profiles-profile-id-filters-filter-filter) |
| [Modify Profile](actions/modify-profile.md) | `PUT /profiles/:profileId` | [docs](https://docs.controld.com/reference/put_profiles-profile-id) |
| [Modify Profile Option](actions/modify-profile-option.md) | `PUT /profiles/:profileId/options/:name` | [docs](https://docs.controld.com/reference/put_profiles-profile-id-options-name) |
| [Modify Profile Service](actions/modify-profile-service.md) | `PUT /profiles/:profileId/services/:service` | [docs](https://docs.controld.com/reference/put_profiles-profile-id-services-service) |
| [Modify Rule Folder](actions/modify-rule-folder.md) | `PUT /profiles/:profileId/groups/:folder` | [docs](https://docs.controld.com/reference/put_profiles-profile-id-groups-folder) |
