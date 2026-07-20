# <img src="https://images.mindcloud.co/apps/icons/images_1773784573320.png" alt="API Template logo" width="28" height="28"> API Template: Universal API

Generate PDFs and images, manage templates, and merge PDFs

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aPITemplate/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apitemplate.io/
- **Vendor API docs:** https://apitemplate.io/apiv2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Account Information](actions/query-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPITemplate/latest/actions/query-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Query Account Information](actions/query-account-information.md) | GET | Retrieves account information from API Template. |

### Generated Object

| Action | Method | Description |
| --- | --- | --- |
| [Delete Object](actions/delete-object.md) | DELETE | Deletes an existing generated object from API Template. |
| [List Generated Objects](actions/list-generated-objects.md) | GET | Retrieves generated objects from API Template. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | POST | Creates an image in API Template. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF](actions/create-pdf.md) | POST | Creates a PDF in API Template. |
| [Create PDF From HTML](actions/create-pdf-from-html.md) | POST | Creates a PDF from HTML in API Template. |
| [Create PDF From URL](actions/create-pdf-from-url.md) | POST | Creates a PDF from a URL in API Template. |
| [Merge PDFs](actions/merge-pdfs.md) | POST | Creates a merged PDF from multiple PDFs in API Template. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a PDF template from API Template. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from API Template. |
| [Update PDF Template](actions/update-pdf-template.md) | PUT | Updates an existing PDF template in API Template. |

