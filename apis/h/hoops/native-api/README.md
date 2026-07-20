# Hoops: Native API Reference

A consolidated summary of Hoops's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.hoop.dev/beta-docs/api-docs
- **API base URL:** `https://use.hoop.dev/api`

## Authentication

### Bearer Access Token

Use a Hoop bearer access token for the managed REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hoop.dev/docs/clients/cli)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent Key](actions/create-agent-key.md) | `POST /agents` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Create Connection](actions/create-connection.md) | `POST /connections` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Create Service Account](actions/create-service-account.md) | `POST /serviceaccounts` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Create Session](actions/create-session.md) | `POST /sessions` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Delete Agent Key](actions/delete-agent-key.md) | `DELETE /agents/{nameOrID}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Delete Connection](actions/delete-connection.md) | `DELETE /connections/{nameOrID}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Delete User](actions/delete-user.md) | `DELETE /users/{id}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Get Connection](actions/get-connection.md) | `GET /connections/{nameOrID}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Get Review](actions/get-review.md) | `GET /reviews/{id}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Get Session](actions/get-session.md) | `GET /sessions/{session_id}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Get User](actions/get-user.md) | `GET /users/{emailOrID}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Get User Info](actions/get-user-info.md) | `GET /userinfo` | [docs](https://docs.hoop.dev/beta-docs/api-docs) |
| [Kill Session](actions/kill-session.md) | `POST /sessions/{session_id}/kill` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [List Agent Keys](actions/list-agent-keys.md) | `GET /agents` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [List Runbooks](actions/list-runbooks.md) | `GET /plugins/runbooks/templates` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [List Service Accounts](actions/list-service-accounts.md) | `GET /serviceaccounts` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Reviewed Exec](actions/reviewed-exec.md) | `POST /sessions/{session_id}/exec` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Runbook Exec](actions/runbook-exec.md) | `POST /runbooks/exec` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Search](actions/search.md) | `GET /search` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Test Connection](actions/test-connection.md) | `GET /connections/{nameOrID}/test` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Update Connection](actions/update-connection.md) | `PUT /connections/{nameOrID}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Update Review Status](actions/update-review-status.md) | `PUT /reviews/{id}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Update Service Account](actions/update-service-account.md) | `PUT /serviceaccounts/{subject}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Update Session Metadata](actions/update-session-metadata.md) | `PATCH /sessions/{session_id}/metadata` | [docs](https://use.hoop.dev/api/openapiv3.json) |
| [Update User](actions/update-user.md) | `PUT /users/{id}` | [docs](https://use.hoop.dev/api/openapiv3.json) |
