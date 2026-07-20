# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-23-as-12_1776957892452.png" alt="Unkey logo" width="28" height="28"> Unkey: Universal API

Manage API keys, identities, roles, and rate limits

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/unkey/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://unkey.com
- **Vendor API docs:** https://unkey.com/docs/api-reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Roles](actions/list-roles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/list-roles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Add key permissions](actions/add-key-permissions.md) | PUT | Adds permissions to an existing API key in Unkey. |
| [Add key roles](actions/add-key-roles.md) | PUT | Adds roles to an existing API key in Unkey. |
| [Create API key](actions/create-api-key.md) | POST | Creates a new API key in Unkey. |
| [Delete API keys](actions/delete-api-keys.md) | DELETE | Deletes an API key from Unkey. |
| [Get API key](actions/get-api-key.md) | GET | Retrieves an API key from Unkey. |
| [Get API key by hash](actions/get-api-key-by-hash.md) | GET | Retrieves an API key from Unkey by hash. |
| [List API keys](actions/list-api-keys.md) | GET | Retrieves API keys from Unkey for an API namespace. |
| [Remove key permissions](actions/remove-key-permissions.md) | PUT | Removes permissions from an existing API key in Unkey. |
| [Remove key roles](actions/remove-key-roles.md) | PUT | Removes roles from an existing API key in Unkey. |
| [Reroll Key](actions/reroll-key.md) | PUT | Rerolls an existing API key in Unkey. |
| [Set key permissions](actions/set-key-permissions.md) | PUT | Sets permissions for an existing API key in Unkey. |
| [Set key roles](actions/set-key-roles.md) | PUT | Sets roles for an existing API key in Unkey. |
| [Update key credits](actions/update-key-credits.md) | PUT | Updates credits for an existing API key in Unkey. |
| [Update key settings](actions/update-key-settings.md) | PUT | Updates settings for an existing API key in Unkey. |
| [Verify API key](actions/verify-api-key.md) | GET | Verifies an API key in Unkey. |

### Api Namespace

| Action | Method | Description |
| --- | --- | --- |
| [Create API namespace](actions/create-api-namespace.md) | POST | Creates a new API namespace in Unkey. |
| [Delete API namespace](actions/delete-api-namespace.md) | DELETE | Deletes an API namespace from Unkey. |
| [Get API namespace](actions/get-api-namespace.md) | GET | Retrieves an API namespace from Unkey. |

### Identity

| Action | Method | Description |
| --- | --- | --- |
| [Create Identity](actions/create-identity.md) | POST | Creates a new identity in Unkey. |
| [Delete Identity](actions/delete-identity.md) | DELETE | Deletes an existing identity from Unkey. |
| [Get Identity](actions/get-identity.md) | GET | Retrieves an identity record from Unkey. |
| [List Identities](actions/list-identities.md) | GET | Retrieves all workspace identities from Unkey. |
| [Update Identity](actions/update-identity.md) | PUT | Updates an existing identity in Unkey. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [Create permission](actions/create-permission.md) | POST | Creates a new permission in Unkey. |
| [Delete permission](actions/delete-permission.md) | DELETE | Deletes an existing permission from Unkey. |
| [Get permission](actions/get-permission.md) | GET | Retrieves a permission record from Unkey. |
| [List permissions](actions/list-permissions.md) | GET | Retrieves all defined permissions from Unkey. |

### Rate Limit Check

| Action | Method | Description |
| --- | --- | --- |
| [Apply multiple rate limit checks](actions/apply-multiple-rate-limit-checks.md) | GET | Applies multiple rate limit checks in Unkey. |
| [Apply rate limiting](actions/apply-rate-limiting.md) | GET | Applies a rate limit check in Unkey. |

### Rate Limit Override

| Action | Method | Description |
| --- | --- | --- |
| [Delete ratelimit override](actions/delete-ratelimit-override.md) | DELETE | Deletes a rate limit override from Unkey. |
| [Get ratelimit override](actions/get-ratelimit-override.md) | GET | Retrieves a rate limit override from Unkey. |
| [List ratelimit overrides](actions/list-ratelimit-overrides.md) | GET | Retrieves rate limit overrides from Unkey. |
| [Set ratelimit override](actions/set-ratelimit-override.md) | PUT | Sets a rate limit override in Unkey. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Create role](actions/create-role.md) | POST | Creates a new role in Unkey. |
| [Delete role](actions/delete-role.md) | DELETE | Deletes an existing role from Unkey. |
| [Get role](actions/get-role.md) | GET | Retrieves a role record from Unkey. |
| [List Roles](actions/list-roles.md) | GET | Retrieves all configured roles from Unkey. |

### Verification Query

| Action | Method | Description |
| --- | --- | --- |
| [Query key verification data](actions/query-key-verification-data.md) | GET | Retrieves key verification data from Unkey. |

