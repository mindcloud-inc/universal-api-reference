# Plaud AI: Native API Reference

A consolidated summary of Plaud AI's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.plaud.ai/plaud-mcp-cli/mcp
- **REST API base URL:** `https://mcp.plaud.ai`
- **REST API base URL:** `https://mcp.plaud.ai`

## Authentication

### OAuth2

Sign in to Plaud to read your synced recordings, transcripts, and notes.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://mcp.plaud.ai/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://mcp.plaud.ai/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


PKCE is enabled with the `other` challenge method. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://mcp.plaud.ai/token.

[Official authentication documentation](https://support.plaud.ai/hc/en-us/articles/57751078986265-Plaud-MCP)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/event-stream` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

- **REST API:** Use `pageSize` in the request body to set the page size (default 20; minimum 10). Use `page` in the request body to choose the page; numbering starts at 1.
- **REST API:** Use `limit` in the request body to set the page size (default 500; accepted range 1–500). Use `cursor` in the request body as the pagination cursor.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `POST /mcp` | [docs](https://docs.plaud.ai/plaud-mcp-cli/mcp) |
| [Get Notes](actions/get-notes.md) | `POST /mcp` | [docs](https://docs.plaud.ai/plaud-mcp-cli/mcp) |
| [Get Recording](actions/get-recording.md) | `POST /mcp` | [docs](https://docs.plaud.ai/plaud-mcp-cli/mcp) |
| [Get Transcript](actions/get-transcript.md) | `POST /mcp` | [docs](https://docs.plaud.ai/plaud-mcp-cli/mcp) |
| [List Recordings](actions/list-recordings.md) | `POST /mcp` | [docs](https://docs.plaud.ai/plaud-mcp-cli/mcp) |
