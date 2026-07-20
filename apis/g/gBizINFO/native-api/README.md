# gBizINFO: Native API Reference

A consolidated summary of gBizINFO's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api.info.gbiz.go.jp/hojin/swagger-ui/index.html
- **OpenAPI specification:** https://api.info.gbiz.go.jp/hojin/v3/api-docs
- **API base URL:** `https://api.info.gbiz.go.jp/hojin`

## Authentication

### API Key

gBizINFO requires the API token in the request header X-hojinInfo-api-token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-hojinInfo-api-token: <apiKey>
```

[Official authentication documentation](https://info.gbiz.go.jp/api-spec/document/policy.pdf)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `hojinInfos`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 0–5000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company (v2)](actions/get-company-v2.md) | `GET /v2/hojin/:corporate_number` | [docs](https://api.info.gbiz.go.jp/hojin/swagger-ui/index.html#/gBizINFO_REST_API/get) |
