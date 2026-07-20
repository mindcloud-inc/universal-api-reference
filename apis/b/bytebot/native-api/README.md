# bytebot: Native API Reference

A consolidated summary of bytebot's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.bytebot.ai/api-reference/introduction
- **OpenAPI specification:** https://raw.githubusercontent.com/bytebot-ai/bytebot/main/docs/api-reference/computer-use/openapi.json
- **API base URL:** `{agentBaseUrl}`

## Authentication

### Bytebot Tenant

Store the tenant-specific Bytebot Desktop API and Agent API base URLs used to run actions against your deployment.

### Credentials

- **Desktop Base URL:** `desktopBaseUrl` · required · Reachable Bytebot Desktop API root URL. Use the service root, not the /computer-use path. Example: http://localhost:9990
- **Agent Base URL:** `agentBaseUrl` · required · Reachable Bytebot Agent API root URL. Use the service root, not the /tasks path. Example: http://localhost:9991

[Official authentication documentation](https://docs.bytebot.ai/api-reference/introduction)

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | `GET {{credentials.agentBaseUrl}}/tasks` | [docs](https://docs.bytebot.ai/api-reference/agent/tasks) |
