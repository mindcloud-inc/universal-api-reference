# Tako: Native API Reference

A consolidated summary of Tako's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.tako.com/documentation/getting-started/overview
- **OpenAPI specification:** https://docs.tako.com/api-reference/openapi.yaml
- **API base URL:** `https://tako.com/api`

## Authentication

### API Key

Use a Tako API key from the Tako dashboard to authenticate API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.tako.com/api-reference/search)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Connect File](actions/connect-file.md) | `POST /v1/beta/file_connector` | [docs](https://docs.tako.com/api-reference/file-connector) |
| [Create Thin-Viz Card](actions/create-thin-viz-card.md) | `POST /v1/thin_viz/create/` | [docs](https://docs.tako.com/api-reference/thinviz-direct-create) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/beta/files/{file_id}/` | [docs](https://docs.tako.com/api-reference/files-delete) |
| [Export Knowledge Card to CSV](actions/export-knowledge-card-to-csv.md) | `GET /v1/csv` | [docs](https://docs.tako.com/api-reference/export-csv) |
| [Export Knowledge Card to PowerPoint](actions/export-knowledge-card-to-power-point.md) | `GET /v1/powerpoint` | [docs](https://docs.tako.com/api-reference/openapi.yaml) |
| [External Query Stream](actions/external-query-stream.md) | `POST /external/v1/query` | [docs](https://docs.tako.com/api-reference/openapi.yaml) |
| [Get Chart Insights](actions/get-chart-insights.md) | `GET /v1/beta/chart_insights` | [docs](https://docs.tako.com/api-reference/insights) |
| [Get File](actions/get-file.md) | `GET /v1/beta/files/{file_id}/` | [docs](https://docs.tako.com/api-reference/files-get) |
| [Get File Upload URL](actions/get-file-upload-url.md) | `GET /v1/beta/file_upload_url` | [docs](https://docs.tako.com/api-reference/file-upload-url) |
| [Get Thin-Viz Default Schema](actions/get-thin-viz-default-schema.md) | `GET /v1/thin_viz/default_schema/{schema_name}/` | [docs](https://docs.tako.com/api-reference/thinviz-default-schema-get) |
| [List Connected Files](actions/list-connected-files.md) | `GET /v1/beta/file_connector` | [docs](https://docs.tako.com/api-reference/file-connector) |
| [List Thin-Viz Default Schemas](actions/list-thin-viz-default-schemas.md) | `GET /v1/thin_viz/default_schema/` | [docs](https://docs.tako.com/api-reference/thinviz-default-schema-list) |
| [List Tool Descriptions](actions/list-tool-descriptions.md) | `GET /v1/tako_tools_description` | [docs](https://docs.tako.com/api-reference/tool-descriptions) |
| [Search Knowledge](actions/search-knowledge.md) | `POST /v1/knowledge_search` | [docs](https://docs.tako.com/api-reference/search) |
| [Search People with Thin-Viz](actions/search-people-with-thin-viz.md) | `POST /v1/thin_viz/search_people/` | [docs](https://docs.tako.com/api-reference/thinviz-search-people) |
| [Visualize Dataset](actions/visualize-dataset.md) | `POST /v1/beta/visualize` | [docs](https://docs.tako.com/api-reference/visualize) |
| [Visualize Dataset Stream](actions/visualize-dataset-stream.md) | `POST /v1/beta/visualize/stream` | [docs](https://docs.tako.com/api-reference/visualize-stream) |
