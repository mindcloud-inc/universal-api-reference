# <img src="https://images.mindcloud.co/apps/icons/p-dfapiio_1774366493738.png" alt="PDF-API.io logo" width="28" height="28"> PDF-API.io: Universal API

Generate PDF documents and manage templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pDFAPIio/latest
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pdf-api.io
- **Vendor API docs:** https://pdf-api.io/en/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFAPIio/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Pdf Document

| Action | Method | Description |
| --- | --- | --- |
| [Merge Templates](actions/merge-templates.md) | POST | Creates one PDF document from multiple templates in PDF-API.io. |
| [Render PDF from Template](actions/render-pdf-from-template.md) | POST | Creates a PDF document from a template in PDF-API.io. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a specific template from PDF-API.io. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from PDF-API.io. |

