# Unkey: Native API Reference

A consolidated summary of Unkey's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://unkey.com/docs/api-reference/overview
- **OpenAPI specification:** https://spec.speakeasy.com/unkey/unkey/openapi-json-with-code-samples
- **API base URL:** `https://api.unkey.com`

## Authentication

### Root Key

Authenticate with an Unkey root key via Authorization bearer auth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.unkey.com/docs/api-reference/v2/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the request body to set the page size. Use `cursor` in the request body as the pagination cursor.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add key permissions](actions/add-key-permissions.md) | `POST /v2/keys.addPermissions` | [docs](https://unkey.com/docs/api-reference/keys/add-key-permissions) |
| [Add key roles](actions/add-key-roles.md) | `POST /v2/keys.addRoles` | [docs](https://unkey.com/docs/api-reference/keys/add-key-roles) |
| [Apply multiple rate limit checks](actions/apply-multiple-rate-limit-checks.md) | `POST /v2/ratelimit.multiLimit` | [docs](https://unkey.com/docs/api-reference/ratelimit/apply-multiple-rate-limit-checks) |
| [Apply rate limiting](actions/apply-rate-limiting.md) | `POST /v2/ratelimit.limit` | [docs](https://unkey.com/docs/api-reference/ratelimit/apply-rate-limiting) |
| [Create API key](actions/create-api-key.md) | `POST /v2/keys.createKey` | [docs](https://unkey.com/docs/api-reference/keys/create-api-key) |
| [Create API namespace](actions/create-api-namespace.md) | `POST /v2/apis.createApi` | [docs](https://unkey.com/docs/api-reference/apis/create-api-namespace) |
| [Create Identity](actions/create-identity.md) | `POST /v2/identities.createIdentity` | [docs](https://unkey.com/docs/api-reference/identities/create-identity) |
| [Create permission](actions/create-permission.md) | `POST /v2/permissions.createPermission` | [docs](https://unkey.com/docs/api-reference/permissions/create-permission) |
| [Create role](actions/create-role.md) | `POST /v2/permissions.createRole` | [docs](https://unkey.com/docs/api-reference/permissions/create-role) |
| [Delete API keys](actions/delete-api-keys.md) | `POST /v2/keys.deleteKey` | [docs](https://unkey.com/docs/api-reference/keys/delete-api-keys) |
| [Delete API namespace](actions/delete-api-namespace.md) | `POST /v2/apis.deleteApi` | [docs](https://unkey.com/docs/api-reference/apis/delete-api-namespace) |
| [Delete Identity](actions/delete-identity.md) | `POST /v2/identities.deleteIdentity` | [docs](https://unkey.com/docs/api-reference/identities/delete-identity) |
| [Delete permission](actions/delete-permission.md) | `POST /v2/permissions.deletePermission` | [docs](https://unkey.com/docs/api-reference/permissions/delete-permission) |
| [Delete ratelimit override](actions/delete-ratelimit-override.md) | `POST /v2/ratelimit.deleteOverride` | [docs](https://unkey.com/docs/api-reference/ratelimit/delete-ratelimit-override) |
| [Delete role](actions/delete-role.md) | `POST /v2/permissions.deleteRole` | [docs](https://unkey.com/docs/api-reference/permissions/delete-role) |
| [Get API key](actions/get-api-key.md) | `POST /v2/keys.getKey` | [docs](https://unkey.com/docs/api-reference/keys/get-api-key) |
| [Get API key by hash](actions/get-api-key-by-hash.md) | `POST /v2/keys.whoami` | [docs](https://unkey.com/docs/api-reference/keys/get-api-key-by-hash) |
| [Get API namespace](actions/get-api-namespace.md) | `POST /v2/apis.getApi` | [docs](https://unkey.com/docs/api-reference/apis/get-api-namespace) |
| [Get Identity](actions/get-identity.md) | `POST /v2/identities.getIdentity` | [docs](https://unkey.com/docs/api-reference/identities/get-identity) |
| [Get permission](actions/get-permission.md) | `POST /v2/permissions.getPermission` | [docs](https://unkey.com/docs/api-reference/permissions/get-permission) |
| [Get ratelimit override](actions/get-ratelimit-override.md) | `POST /v2/ratelimit.getOverride` | [docs](https://unkey.com/docs/api-reference/ratelimit/get-ratelimit-override) |
| [Get role](actions/get-role.md) | `POST /v2/permissions.getRole` | [docs](https://unkey.com/docs/api-reference/permissions/get-role) |
| [List API keys](actions/list-api-keys.md) | `POST /v2/apis.listKeys` | [docs](https://unkey.com/docs/api-reference/apis/list-api-keys) |
| [List Identities](actions/list-identities.md) | `POST /v2/identities.listIdentities` | [docs](https://unkey.com/docs/api-reference/identities/list-identities) |
| [List permissions](actions/list-permissions.md) | `POST /v2/permissions.listPermissions` | [docs](https://unkey.com/docs/api-reference/permissions/list-permissions) |
| [List ratelimit overrides](actions/list-ratelimit-overrides.md) | `POST /v2/ratelimit.listOverrides` | [docs](https://unkey.com/docs/api-reference/ratelimit/list-ratelimit-overrides) |
| [List Roles](actions/list-roles.md) | `POST /v2/permissions.listRoles` | [docs](https://unkey.com/docs/api-reference/permissions/list-roles) |
| [Query key verification data](actions/query-key-verification-data.md) | `POST /v2/analytics.getVerifications` | [docs](https://unkey.com/docs/api-reference/analytics/query-key-verification-data) |
| [Remove key permissions](actions/remove-key-permissions.md) | `POST /v2/keys.removePermissions` | [docs](https://unkey.com/docs/api-reference/keys/remove-key-permissions) |
| [Remove key roles](actions/remove-key-roles.md) | `POST /v2/keys.removeRoles` | [docs](https://unkey.com/docs/api-reference/keys/remove-key-roles) |
| [Reroll Key](actions/reroll-key.md) | `POST /v2/keys.rerollKey` | [docs](https://unkey.com/docs/api-reference/keys/reroll-key) |
| [Set key permissions](actions/set-key-permissions.md) | `POST /v2/keys.setPermissions` | [docs](https://unkey.com/docs/api-reference/keys/set-key-permissions) |
| [Set key roles](actions/set-key-roles.md) | `POST /v2/keys.setRoles` | [docs](https://unkey.com/docs/api-reference/keys/set-key-roles) |
| [Set ratelimit override](actions/set-ratelimit-override.md) | `POST /v2/ratelimit.setOverride` | [docs](https://unkey.com/docs/api-reference/ratelimit/set-ratelimit-override) |
| [Update Identity](actions/update-identity.md) | `POST /v2/identities.updateIdentity` | [docs](https://unkey.com/docs/api-reference/identities/update-identity) |
| [Update key credits](actions/update-key-credits.md) | `POST /v2/keys.updateCredits` | [docs](https://unkey.com/docs/api-reference/keys/update-key-credits) |
| [Update key settings](actions/update-key-settings.md) | `POST /v2/keys.updateKey` | [docs](https://unkey.com/docs/api-reference/keys/update-key-settings) |
| [Verify API key](actions/verify-api-key.md) | `POST /v2/keys.verifyKey` | [docs](https://unkey.com/docs/api-reference/keys/verify-api-key) |
