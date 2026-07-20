# <img src="https://images.mindcloud.co/apps/icons/craft-my-pdf_1773343667860.png" alt="CraftMyPDF logo" width="28" height="28"> CraftMyPDF: Universal API

Create PDFs and images, manage templates, and edit documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/craftMyPDF/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://craftmypdf.com
- **Vendor API docs:** https://craftmypdf.com/docs/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get account information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get account information](actions/get-account-information.md) | GET | Retrieves account information from your CraftMyPDF account. |

### Editor Session

| Action | Method | Description |
| --- | --- | --- |
| [Create editor session](actions/create-editor-session.md) | POST | Creates an editor session in CraftMyPDF. |
| [Deactivate editor session](actions/deactivate-editor-session.md) | PUT | Deactivates an editor session in CraftMyPDF. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Create an image](actions/create-an-image.md) | POST | Creates an image file in CraftMyPDF. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Add text to a PDF](actions/add-text-to-apdf.md) | PUT | Adds text to a PDF in CraftMyPDF. |
| [Add watermark to a PDF](actions/add-watermark-to-apdf.md) | PUT | Adds a watermark to a PDF in CraftMyPDF. |
| [Create a PDF](actions/create-apdf.md) | POST | Creates a PDF document in CraftMyPDF. |
| [Create a PDF asynchronously](actions/create-apdf-asynchronously.md) | POST | Creates a PDF asynchronously in CraftMyPDF. |
| [Create PDFs parallelly](actions/create-pd-fs-parallelly.md) | POST | Creates multiple PDFs in parallel in CraftMyPDF. |
| [Create PDF from templates](actions/create-pdf-from-templates.md) | POST | Creates a PDF from templates in CraftMyPDF. |
| [Get PDF Information](actions/get-pdf-information.md) | GET | Retrieves PDF file information from CraftMyPDF. |
| [Merge PDF URLs](actions/merge-pdfur-ls.md) | POST | Merges PDF files from URLs in CraftMyPDF. |
| [Update fillable fields](actions/update-fillable-fields.md) | PUT | Updates fillable PDF fields in CraftMyPDF. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create a new template](actions/create-a-new-template.md) | POST | Creates a new template in CraftMyPDF. |
| [Delete template](actions/delete-template.md) | DELETE | Deletes a template record from CraftMyPDF. |
| [Get template](actions/get-template.md) | GET | Retrieves a template record from CraftMyPDF. |
| [List templates](actions/list-templates.md) | GET | Retrieves templates from your CraftMyPDF account. |
| [Transfer a template](actions/transfer-a-template.md) | PUT | Transfers a template to another CraftMyPDF account. |
| [Update template](actions/update-template.md) | PUT | Updates an existing template in CraftMyPDF. |

### Template Usage

| Action | Method | Description |
| --- | --- | --- |
| [Query template usage](actions/query-template-usage.md) | GET | Retrieves template usage details from CraftMyPDF. |

### Template Version

| Action | Method | Description |
| --- | --- | --- |
| [List template versions](actions/list-template-versions.md) | GET | Retrieves template versions from your CraftMyPDF account. |
| [Retain template versions](actions/retain-template-versions.md) | PUT | Updates retained template versions in CraftMyPDF. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List transactions](actions/list-transactions.md) | GET | Retrieves transactions from your CraftMyPDF account. |

