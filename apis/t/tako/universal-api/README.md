# <img src="https://images.mindcloud.co/apps/icons/tako_1776959201839.png" alt="Tako logo" width="28" height="28"> Tako: Universal API

Tako is a search engine for visualizing and sharing the world's knowledge. This wrapper exposes Tako's stable API-key-authenticated search, visualization, export, file, and thin-viz endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tako/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tako.com
- **Vendor API docs:** https://docs.tako.com/documentation/getting-started/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tool Descriptions](actions/list-tool-descriptions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-tool-descriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Connect File](actions/connect-file.md) | POST | Connects a file to Tako for analysis. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Tako. |
| [Get File](actions/get-file.md) | GET | Retrieves file metadata from Tako. |
| [Get File Upload URL](actions/get-file-upload-url.md) | GET | Retrieves a file upload URL from Tako. |
| [List Connected Files](actions/list-connected-files.md) | GET | Retrieves connected files from Tako. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [External Query Stream](actions/external-query-stream.md) | GET | Streams external query results from Tako. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create Thin-Viz Card](actions/create-thin-viz-card.md) | POST | Creates an embeddable Thin-Viz card in Tako. |
| [Export Knowledge Card to CSV](actions/export-knowledge-card-to-csv.md) | GET | Exports a Tako knowledge card to CSV. |
| [Export Knowledge Card to PowerPoint](actions/export-knowledge-card-to-power-point.md) | GET | Exports a Tako knowledge card to PowerPoint. |
| [Get Chart Insights](actions/get-chart-insights.md) | GET | Retrieves insights from a Tako knowledge card chart. |
| [Search Knowledge](actions/search-knowledge.md) | GET | Searches Tako Knowledge Cards with natural language. |
| [Visualize Dataset](actions/visualize-dataset.md) | POST | Creates a knowledge card from your dataset in Tako. |
| [Visualize Dataset Stream](actions/visualize-dataset-stream.md) | POST | Creates a knowledge card from your dataset in Tako as a stream. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Tool Descriptions](actions/list-tool-descriptions.md) | GET | Retrieves tool descriptions from Tako. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Thin-Viz Default Schema](actions/get-thin-viz-default-schema.md) | GET | Retrieves a Thin-Viz default schema from Tako. |
| [List Thin-Viz Default Schemas](actions/list-thin-viz-default-schemas.md) | GET | Retrieves Thin-Viz default schemas from Tako. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Search People with Thin-Viz](actions/search-people-with-thin-viz.md) | POST | Searches people with Thin-Viz in Tako. |

