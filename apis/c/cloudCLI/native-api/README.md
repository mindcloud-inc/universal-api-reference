# Cloud CLI: Native API Reference

A consolidated summary of Cloud CLI's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developer.cloudcli.ai/
- **API base URL:** `https://cloudcli.ai/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developer.cloudcli.ai/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Environment](actions/create-environment.md) | `POST /environments` | [docs](https://developer.cloudcli.ai/create-environment-3998768e0) |
| [Delete Environment](actions/delete-environment.md) | `DELETE /environments/:id` | [docs](https://developer.cloudcli.ai/delete-environment-3998770e0) |
| [Execute AI Agent](actions/execute-ai-agent.md) | `POST /agent/execute` | [docs](https://developer.cloudcli.ai/execute-ai-agent-3998774e0) |
| [Get Environment](actions/get-environment.md) | `GET /environments/:id` | [docs](https://developer.cloudcli.ai/get-environment-3998769e0) |
| [Get SSH Credentials](actions/get-ssh-credentials.md) | `GET /environments/:id/credentials` | [docs](https://developer.cloudcli.ai/get-ssh-credentials-3998773e0) |
| [List AI Agent Models](actions/list-ai-agent-models.md) | `GET /agent/models` | [docs](https://developer.cloudcli.ai/ai-agent-models-4026679e0) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://developer.cloudcli.ai/list-environments-3998767e0) |
| [Start Environment](actions/start-environment.md) | `POST /environments/:id/start` | [docs](https://developer.cloudcli.ai/start-environment-3998771e0) |
| [Stop Environment](actions/stop-environment.md) | `POST /environments/:id/stop` | [docs](https://developer.cloudcli.ai/stop-environment-3998772e0) |
