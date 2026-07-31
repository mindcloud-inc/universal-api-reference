# Excuser: Native API Reference

A consolidated summary of Excuser's API configuration and 5 documented operations.

- **API base URL:** `https://excuser-three.vercel.app`

## Authentication

### No Authentication

This API does not require request authentication.

[Official authentication documentation](https://excuser-three.vercel.app/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Fetch Excuse By ID](actions/fetch-excuse-by-id.md) | `GET /v1/excuse/id/:id` | [docs](https://excuser-three.vercel.app/) |
| [Fetch Random Excuse](actions/fetch-random-excuse.md) | `GET /v1/excuse` | [docs](https://excuser-three.vercel.app/) |
| [Fetch Random Excuse By Category](actions/fetch-random-excuse-by-category.md) | `GET /v1/excuse/:category` | [docs](https://excuser-three.vercel.app/) |
| [Fetch Random Excuses](actions/fetch-random-excuses.md) | `GET /v1/excuse/:count` | [docs](https://excuser-three.vercel.app/) |
| [Fetch Random Excuses By Category](actions/fetch-random-excuses-by-category.md) | `GET /v1/excuse/:category/:count` | [docs](https://excuser-three.vercel.app/) |
