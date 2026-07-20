# <img src="https://images.mindcloud.co/apps/icons/columns-ai_1776171941176.png" alt="Columns AI logo" width="28" height="28"> Columns AI: Universal API

Create, publish, and download Columns visualizations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/columnsAI/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://columns.ai
- **Vendor API docs:** https://github.com/varchar-io/vaas

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Visual Template](actions/get-visual-template.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/get-visual-template?connectionId=$CONNECTION_ID&id=U6tALuJ3cTdPFw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Graph

| Action | Method | Description |
| --- | --- | --- |
| [Publish Graph](actions/publish-graph.md) | POST | Publishes a graph to Columns AI. |

### Graph Image

| Action | Method | Description |
| --- | --- | --- |
| [Download Graph Image](actions/download-graph-image.md) | GET | Downloads a graph image from Columns AI by visual ID. |

### Visual Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Visual Template](actions/get-visual-template.md) | GET | Retrieves a visual template from Columns AI by visual ID. |

