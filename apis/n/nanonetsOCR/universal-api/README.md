# <img src="https://images.mindcloud.co/apps/icons/id4m-fvwy15-logos_1773857838916.png" alt="Nanonets OCR logo" width="28" height="28"> Nanonets OCR: Universal API

Extract document data and automate OCR workflows with Nanonets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nanonetsOCR/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nanonets.com
- **Vendor API docs:** https://apidocs.nanonets.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available Workflow Types](actions/list-available-workflow-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-available-workflow-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Get Document Data](actions/get-document-data.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |
| [Upload Document For Processing](actions/upload-document-for-processing.md) | POST |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Data](actions/get-page-data.md) | GET |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST |  |
| [Get Workflow](actions/get-workflow.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |
| [Set Fields And Table Headers](actions/set-fields-and-table-headers.md) | PUT |  |

### Workflow Field

| Action | Method | Description |
| --- | --- | --- |
| [Delete Field Or Table Header](actions/delete-field-or-table-header.md) | DELETE |  |
| [Update Field Or Table Header](actions/update-field-or-table-header.md) | PUT |  |

### Workflow Type

| Action | Method | Description |
| --- | --- | --- |
| [List Available Workflow Types](actions/list-available-workflow-types.md) | GET |  |

