# <img src="https://images.mindcloud.co/apps/icons/docmosis_1774454445811.png" alt="Docmosis logo" width="28" height="28"> Docmosis: Universal API

Generate documents and manage Docmosis templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docmosis/latest
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docmosis.com/document-generation-software/cloud/
- **Vendor API docs:** https://apidocs.docmosis.com/cloud/dws4/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Environment Summary](actions/get-environment-summary.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-environment-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert File](actions/convert-file.md) | POST |  |
| [Render Documents](actions/render-documents.md) | POST |  |

### Environment

| Action | Method | Description |
| --- | --- | --- |
| [Get Environment Ready Status](actions/get-environment-ready-status.md) | GET |  |
| [Get Environment Summary](actions/get-environment-summary.md) | GET |  |
| [Ping](actions/ping.md) | GET |  |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Delete Image](actions/delete-image.md) | DELETE |  |
| [Get Image](actions/get-image.md) | GET |  |
| [List Images](actions/list-images.md) | GET |  |
| [Upload Image](actions/upload-image.md) | POST |  |

### Render Queue

| Action | Method | Description |
| --- | --- | --- |
| [Get Render Queue](actions/get-render-queue.md) | GET |  |

### Render Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Render Tags](actions/get-render-tags.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Delete Template](actions/delete-template.md) | DELETE |  |
| [Get Template](actions/get-template.md) | GET |  |
| [Get Template Details](actions/get-template-details.md) | GET |  |
| [Get Template Sample Data](actions/get-template-sample-data.md) | GET |  |
| [Get Template Structure](actions/get-template-structure.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [Upload Template](actions/upload-template.md) | POST |  |

### Template Batch

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Upload Template Batch](actions/cancel-upload-template-batch.md) | DELETE |  |
| [Get Upload Template Batch Status](actions/get-upload-template-batch-status.md) | GET |  |
| [Upload Template Batch](actions/upload-template-batch.md) | POST |  |

