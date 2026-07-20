# Remote OK: Native API Reference

A consolidated summary of Remote OK's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://remoteok.com/json
- **API base URL:** `https://remoteok.com`

## Authentication

### No auth

Remote OK exposes a public JSON jobs feed without authentication.

This API does not require request authentication.

[Official authentication documentation](https://remoteok.com/json)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json,text/plain,*/*` |
| `User-Agent` | `Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/123 Safari/537.36` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Remote Jobs](actions/list-remote-jobs.md) | `GET /api` | [docs](https://remoteok.com/json) |
