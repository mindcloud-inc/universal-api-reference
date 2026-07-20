# Make: Native API Reference

A consolidated summary of Make's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.make.com/api-documentation
- **API base URL:** `https://us2.make.com/api/v2`

## Authentication

### API Token

Authenticate Make API requests with a Make API token sent in the Authorization header as `Token <api-token>`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.make.com/api-documentation/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Scenario Folder](actions/create-scenario-folder.md) | `POST /scenarios-folders` | [docs](https://developers.make.com/api-documentation/api-reference/scenarios-folders) |
| [Get Current Authorization](actions/get-current-authorization.md) | `GET /users/me/current-authorization` | [docs](https://developers.make.com/api-documentation/api-reference/users-greater-than-me) |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://developers.make.com/api-documentation/api-reference/users) |
| [List AI Agents](actions/list-ai-agents.md) | `GET /ai-agents/v1/agents` | [docs](https://developers.make.com/api-documentation/api-reference/ai-agents) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://developers.make.com/api-documentation/api-reference/connections) |
| [List Credential Requests](actions/list-credential-requests.md) | `GET /credential-requests/requests` | [docs](https://developers.make.com/api-documentation/api-reference/credential-requests) |
| [List Custom Property Structures](actions/list-custom-property-structures.md) | `GET /custom-property-structures` | [docs](https://developers.make.com/api-documentation/api-reference/custom-property-structures) |
| [List Data Stores](actions/list-data-stores.md) | `GET /data-stores` | [docs](https://developers.make.com/api-documentation/api-reference/data-stores) |
| [List Data Structures](actions/list-data-structures.md) | `GET /data-structures` | [docs](https://developers.make.com/api-documentation/api-reference/data-structures) |
| [List Devices](actions/list-devices.md) | `GET /devices` | [docs](https://developers.make.com/api-documentation/api-reference/devices) |
| [List Hooks](actions/list-hooks.md) | `GET /hooks` | [docs](https://developers.make.com/api-documentation/api-reference/hooks) |
| [List Keys](actions/list-keys.md) | `GET /keys` | [docs](https://developers.make.com/api-documentation/api-reference/keys) |
| [List LLM Providers](actions/list-llm-providers.md) | `GET /ai-agents/v1/llm-providers` | [docs](https://developers.make.com/api-documentation/api-reference/ai-agents) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://developers.make.com/api-documentation/api-reference/notifications) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developers.make.com/api-documentation/api-reference/organizations) |
| [List Scenario Folders](actions/list-scenario-folders.md) | `GET /scenarios-folders` | [docs](https://developers.make.com/api-documentation/api-reference/scenarios-folders) |
| [List Scenarios](actions/list-scenarios.md) | `GET /scenarios` | [docs](https://developers.make.com/api-documentation/api-reference/scenarios) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://developers.make.com/api-documentation/api-reference/teams) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://developers.make.com/api-documentation/api-reference/templates) |
| [List User Roles](actions/list-user-roles.md) | `GET /users/roles` | [docs](https://developers.make.com/api-documentation/api-reference/users) |
