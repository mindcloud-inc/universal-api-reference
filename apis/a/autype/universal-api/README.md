# <img src="https://images.mindcloud.co/apps/icons/autype_1777387202853.png" alt="Autype logo" width="28" height="28"> Autype: Universal API

Autype Developer API for programmatic document generation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/autype/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://autype.com
- **Vendor API docs:** https://docs.autype.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Key Info](actions/get-api-key-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autype/latest/actions/get-api-key-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Get API Key Info](actions/get-api-key-info.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Autype. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Autype. |
| [Get Document Variables](actions/get-document-variables.md) | GET | Retrieves document variables from Autype. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Autype. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Validate Document JSON](actions/validate-document-json.md) | GET | Validates document JSON content in Autype. |
| [Validate Markdown](actions/validate-markdown.md) | GET | Validates document markdown content in Autype. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing tool file from Autype. |
| [Delete Temporary Image](actions/delete-temporary-image.md) | DELETE | Deletes a temporary image from Autype. |
| [Download File](actions/download-file.md) | GET | Downloads a tool file from Autype. |
| [Get File Details](actions/get-file-details.md) | GET | Retrieves tool file details from Autype. |
| [List Files](actions/list-files.md) | GET | Retrieves tool files from Autype. |
| [List Temporary Images](actions/list-temporary-images.md) | GET | Retrieves temporary images from Autype. |
| [Upload File](actions/upload-file.md) | POST | Uploads a tool file to Autype. |
| [Upload Temporary Image](actions/upload-temporary-image.md) | POST | Uploads a temporary image to Autype. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [List Render Jobs](actions/list-render-jobs.md) | GET | Retrieves render jobs from Autype. |
| [Render Document](actions/render-document.md) | POST | Creates a temporary document render job from JSON in Autype. |
| [Render Markdown](actions/render-markdown.md) | POST | Creates a temporary document render job from markdown in Autype. |
| [Render Persistent Document](actions/render-persistent-document.md) | POST | Creates a persistent document render job in Autype. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Render Job From File](actions/create-bulk-render-job-from-file.md) | POST | Creates a bulk render job from a file in Autype. |
| [Create Bulk Render Job From JSON](actions/create-bulk-render-job-from-json.md) | POST | Creates a bulk render job from JSON in Autype. |
| [Download Bulk Render Output ZIP](actions/download-bulk-render-output-zip.md) | GET | Downloads a bulk render output ZIP from Autype. |
| [Download Render Output File](actions/download-render-output-file.md) | GET | Downloads a render output file from Autype. |
| [Get Bulk Render Job Status](actions/get-bulk-render-job-status.md) | GET | Retrieves bulk render job status from Autype. |
| [Get Render Job Status](actions/get-render-job-status.md) | GET | Retrieves render job status from Autype. |
| [Merge PDFs](actions/merge-pdfs.md) | POST | Creates a PDF merge job in Autype. |
| [Rotate PDF Pages](actions/rotate-pdf-pages.md) | POST | Creates a PDF rotation job in Autype. |
| [Split PDF](actions/split-pdf.md) | POST | Creates a PDF split job in Autype. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Autype. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Autype. |

