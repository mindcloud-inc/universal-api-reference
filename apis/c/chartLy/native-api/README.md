# ChartLy: Native API Reference

A consolidated summary of ChartLy's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://docs.chartly.dev/api
- **OpenAPI specification:** https://api.chartly.dev/openapi.json
- **API base URL:** `https://api.chartly.dev`

## Authentication

### API Key

Connect ChartLy with your API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.chartly.dev/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bar Chart (Zapier)](actions/create-bar-chart-zapier.md) | `POST /v1/zapier/bar-chart` | [docs](https://docs.chartly.dev/api/) |
| [Create Line Chart (Zapier)](actions/create-line-chart-zapier.md) | `POST /v1/zapier/line-chart` | [docs](https://docs.chartly.dev/api/) |
| [Create Multi-Series Chart (Zapier)](actions/create-multi-series-chart-zapier.md) | `POST /v1/zapier/multi-series-chart` | [docs](https://docs.chartly.dev/api/) |
| [Create Permanent Signed Short URL](actions/create-permanent-signed-short-url.md) | `POST /v1/chart/create` | [docs](https://docs.chartly.dev/api#post-v1chartcreate) |
| [Create Pie Chart (Zapier)](actions/create-pie-chart-zapier.md) | `POST /v1/zapier/pie-chart` | [docs](https://docs.chartly.dev/api/) |
| [Get Status](actions/get-status.md) | `GET /v1/status` | [docs](https://docs.chartly.dev/api#get-v1status) |
| [Render Chart From JSON](actions/render-chart-from-json.md) | `POST /v1/chart` | [docs](https://docs.chartly.dev/api#post-v1chart) |
| [Render Chart From URL](actions/render-chart-from-url.md) | `GET /v1/chart` | [docs](https://docs.chartly.dev/api#get-v1chart) |
