# Confluent: Native API Reference

A consolidated summary of Confluent's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.confluent.io/cloud/current/api.html
- **API base URL:** `https://api.confluent.cloud`

## Authentication

### Basic

Authenticate with your Confluent Cloud API key as the username and API secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.confluent.io/cloud/current/security/authenticate/workload-identities/service-accounts/api-keys/overview.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100). Use `page_token` in the query string as the pagination cursor.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | `POST /iam/v2/api-keys` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/createIamV2ApiKey) |
| [Create Environment](actions/create-environment.md) | `POST /org/v2/environments` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Environments-(orgv2)/operation/createOrgV2Environment) |
| [Create IP Filter](actions/create-ip-filter.md) | `POST /iam/v2/ip-filters` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/createIamV2IpFilter) |
| [Create IP Group](actions/create-ip-group.md) | `POST /iam/v2/ip-groups` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Groups-(iamv2)/operation/createIamV2IpGroup) |
| [Create Service Account](actions/create-service-account.md) | `POST /iam/v2/service-accounts` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/createIamV2ServiceAccount) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /iam/v2/api-keys/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/deleteIamV2ApiKey) |
| [Delete Environment](actions/delete-environment.md) | `DELETE /org/v2/environments/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Environments-(orgv2)/operation/deleteOrgV2Environment) |
| [Delete IP Filter](actions/delete-ip-filter.md) | `DELETE /iam/v2/ip-filters/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/deleteIamV2IpFilter) |
| [Delete IP Group](actions/delete-ip-group.md) | `DELETE /iam/v2/ip-groups/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Groups-(iamv2)/operation/deleteIamV2IpGroup) |
| [Delete Service Account](actions/delete-service-account.md) | `DELETE /iam/v2/service-accounts/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/deleteIamV2ServiceAccount) |
| [List API Keys](actions/list-api-keys.md) | `GET /iam/v2/api-keys` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/listIamV2ApiKeys) |
| [List Environments](actions/list-environments.md) | `GET /org/v2/environments` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Environments-(orgv2)/operation/listOrgV2Environments) |
| [List IP Filters](actions/list-ip-filters.md) | `GET /iam/v2/ip-filters` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/listIamV2IpFilters) |
| [List IP Groups](actions/list-ip-groups.md) | `GET /iam/v2/ip-groups` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Groups-(iamv2)/operation/listIamV2IpGroups) |
| [List Organizations](actions/list-organizations.md) | `GET /org/v2/organizations` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Organizations-(orgv2)/operation/listOrgV2Organizations) |
| [List Role Bindings](actions/list-role-bindings.md) | `GET /iam/v2/role-bindings` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Role-Bindings-(iamv2)/operation/listIamV2RoleBindings) |
| [List Service Accounts](actions/list-service-accounts.md) | `GET /iam/v2/service-accounts` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/listIamV2ServiceAccounts) |
| [List Users](actions/list-users.md) | `GET /iam/v2/users` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Users-(iamv2)/operation/listIamV2Users) |
| [Read API Key](actions/read-api-key.md) | `GET /iam/v2/api-keys/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/getIamV2ApiKey) |
| [Read Environment](actions/read-environment.md) | `GET /org/v2/environments/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Environments-(orgv2)/operation/getOrgV2Environment) |
| [Read IP Filter](actions/read-ip-filter.md) | `GET /iam/v2/ip-filters/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/getIamV2IpFilter) |
| [Read IP Group](actions/read-ip-group.md) | `GET /iam/v2/ip-groups/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Groups-(iamv2)/operation/getIamV2IpGroup) |
| [Read Organization](actions/read-organization.md) | `GET /org/v2/organizations/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Organizations-(orgv2)/operation/getOrgV2Organization) |
| [Read Role Binding](actions/read-role-binding.md) | `GET /iam/v2/role-bindings/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Role-Bindings-(iamv2)/operation/getIamV2RoleBinding) |
| [Read Service Account](actions/read-service-account.md) | `GET /iam/v2/service-accounts/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/getIamV2ServiceAccount) |
| [Read User](actions/read-user.md) | `GET /iam/v2/users/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Users-(iamv2)/operation/getIamV2User) |
| [Update API Key](actions/update-api-key.md) | `PATCH /iam/v2/api-keys/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/updateIamV2ApiKey) |
| [Update Environment](actions/update-environment.md) | `PATCH /org/v2/environments/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Environments-(orgv2)/operation/updateOrgV2Environment) |
| [Update IP Filter](actions/update-ip-filter.md) | `PATCH /iam/v2/ip-filters/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Filters-(iamv2)/operation/updateIamV2IpFilter) |
| [Update IP Group](actions/update-ip-group.md) | `PATCH /iam/v2/ip-groups/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/IP-Groups-(iamv2)/operation/updateIamV2IpGroup) |
| [Update Service Account](actions/update-service-account.md) | `PATCH /iam/v2/service-accounts/:id` | [docs](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/updateIamV2ServiceAccount) |
