# <img src="https://images.mindcloud.co/apps/icons/stencil_1774887155385.png" alt="Stencil logo" width="28" height="28"> Stencil: Universal API

Generate, search, and manage images, PDFs, and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stencil/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://usestencil.com
- **Vendor API docs:** https://docs.usestencil.com/api/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Airtable Generation

| Action | Method | Description |
| --- | --- | --- |
| [Get Airtable Image Generation Status](actions/get-airtable-image-generation-status.md) | GET |  |
| [Trigger Airtable Image Generation](actions/trigger-airtable-image-generation.md) | PUT |  |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection Images](actions/create-collection-images.md) | POST |  |
| [Retrieve Collection Images](actions/retrieve-collection-images.md) | GET |  |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | POST |  |
| [Create Image Synchronously](actions/create-image-synchronously.md) | POST |  |
| [Search Images](actions/search-images.md) | GET |  |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF](actions/create-pdf.md) | POST |  |
| [Get PDF](actions/get-pdf.md) | GET |  |
| [Search PDFs](actions/search-pdfs.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Editor Session](actions/create-editor-session.md) | POST |  |
| [Get Editor Session](actions/get-editor-session.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

