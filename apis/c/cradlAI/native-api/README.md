# Cradl AI: Native API Reference

A consolidated summary of Cradl AI's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.cradl.ai/api-reference/introduction
- **API base URL:** `https://api.cradl.ai/v1`

## Authentication

### OAuth2

Cradl uses OAuth2 client_credentials. Sign up for Cradl, then get the client ID and client secret from the Cradl AI app and enter them in the connection.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://auth.cradl.ai/oauth2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.cradl.ai/api-reference/introduction)

## API conventions

Response data is read from `agents`. The next-page cursor is read from `nextToken`.

## Pagination

Use `maxResults` in the query string to set the page size. Use `nextToken` in the query string as the pagination cursor.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Agent](actions/create-agent.md) | `POST /agents` | [docs](https://docs.cradl.ai/api-reference/post-agents) |
| [Create Agent Run](actions/create-agent-run.md) | `POST /agents/:agentId/runs` | [docs](https://docs.cradl.ai/api-reference/post-agents-runs) |
| [Create Document](actions/create-document.md) | `POST /documents` | [docs](https://docs.cradl.ai/api-reference/post-documents) |
| [Create Function](actions/create-function.md) | `POST /functions` | [docs](https://docs.cradl.ai/api-reference/post-functions) |
| [Create Hook](actions/create-hook.md) | `POST /hooks` | [docs](https://docs.cradl.ai/api-reference/post-hooks) |
| [Delete Agent](actions/delete-agent.md) | `DELETE /agents/:agentId` | [docs](https://docs.cradl.ai/api-reference/delete-agents) |
| [Delete Agent Run](actions/delete-agent-run.md) | `DELETE /agents/:agentId/runs/:runId` | [docs](https://docs.cradl.ai/api-reference/delete-agents-runs) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:documentId` | [docs](https://docs.cradl.ai/api-reference/delete-documents) |
| [Delete Function](actions/delete-function.md) | `DELETE /functions/:functionId` | [docs](https://docs.cradl.ai/api-reference/delete-functions) |
| [Delete Hook](actions/delete-hook.md) | `DELETE /hooks/:hookId` | [docs](https://docs.cradl.ai/api-reference/delete-hooks) |
| [Get Agent](actions/get-agent.md) | `GET /agents/:agentId` | [docs](https://docs.cradl.ai/api-reference/get-agents-1) |
| [Get Agent Run](actions/get-agent-run.md) | `GET /agents/:agentId/runs/:runId` | [docs](https://docs.cradl.ai/api-reference/get-agents-runs-1) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://docs.cradl.ai/api-reference/get-documents-1) |
| [Get Function](actions/get-function.md) | `GET /functions/:functionId` | [docs](https://docs.cradl.ai/api-reference/get-functions-1) |
| [Get Hook](actions/get-hook.md) | `GET /hooks/:hookId` | [docs](https://docs.cradl.ai/api-reference/get-hooks-1) |
| [List Agent Runs](actions/list-agent-runs.md) | `GET /agents/:agentId/runs` | [docs](https://docs.cradl.ai/api-reference/get-agents-runs) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://docs.cradl.ai/api-reference/get-agents) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.cradl.ai/api-reference/get-documents) |
| [List Functions](actions/list-functions.md) | `GET /functions` | [docs](https://docs.cradl.ai/api-reference/get-functions) |
| [List Hooks](actions/list-hooks.md) | `GET /hooks` | [docs](https://docs.cradl.ai/api-reference/get-hooks) |
| [Update Agent](actions/update-agent.md) | `PATCH /agents/:agentId` | [docs](https://docs.cradl.ai/api-reference/patch-agents) |
| [Update Agent Run](actions/update-agent-run.md) | `PATCH /agents/:agentId/runs/:runId` | [docs](https://docs.cradl.ai/api-reference/patch-agents-runs) |
| [Update Document](actions/update-document.md) | `PATCH /documents/:documentId` | [docs](https://docs.cradl.ai/api-reference/patch-documents) |
| [Update Function](actions/update-function.md) | `PATCH /functions/:functionId` | [docs](https://docs.cradl.ai/api-reference/patch-functions) |
| [Update Hook](actions/update-hook.md) | `PATCH /hooks/:hookId` | [docs](https://docs.cradl.ai/api-reference/patch-hooks) |
