# <img src="https://images.mindcloud.co/apps/icons/text-to-pdf-icon_1776707581673.png" alt="Text to pdf logo" width="28" height="28"> Text to pdf: Universal API

Convert text and Markdown into PDF files, and manage temporary Text to PDF conversion jobs and files through Composio.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/textToPdf/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://composio.dev/toolkits/text_to_pdf
- **Vendor API docs:** https://docs.composio.dev/toolkits/text_to_pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download File](actions/download-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/textToPdf/latest/actions/download-file?connectionId=$CONNECTION_ID&arguments=%5Bobject%20Object%5D&arguments.fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert Text to PDF](actions/convert-text-to-pdf.md) | POST | Creates a PDF document from text in Text to PDF. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from Text to PDF by file ID. |
| [Download File](actions/download-file.md) | GET | Retrieves a file from Text to PDF by file ID. |
| [Upload File to ConvertAPI](actions/upload-file-to-convert-api.md) | POST | Uploads a file to Text to PDF for later conversion. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Async Job](actions/delete-async-job.md) | DELETE | Deletes an asynchronous job from Text to PDF. |
| [Start Async Conversion](actions/start-async-conversion.md) | POST | Starts an asynchronous file conversion job in Text to PDF. |

