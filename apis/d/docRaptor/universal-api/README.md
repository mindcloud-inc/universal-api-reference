# <img src="https://images.mindcloud.co/apps/icons/docraptor-icon_1778011576702.png" alt="DocRaptor logo" width="28" height="28"> DocRaptor: Universal API

DocRaptor converts HTML into PDF, XLS, and XLSX documents through a REST API, including synchronous, asynchronous, and hosted document workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docRaptor/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docraptor.com
- **Vendor API docs:** https://docraptor.com/documentation/api/making_documents

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Async Document Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Document Status](actions/get-async-document-status.md) | GET | Retrieves async document job status from DocRaptor. |

### Async Pdf Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Async PDF from HTML Content](actions/create-async-pdf-from-html-content.md) | POST | Creates an async PDF in DocRaptor from HTML content. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Retrieves paginated document records from DocRaptor. |

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [List DocRaptor IP Addresses](actions/list-docraptor-ip-addresses.md) | GET | Retrieves the current DocRaptor IP addresses. |

### Pdf Document

| Action | Method | Description |
| --- | --- | --- |
| [Create PDF from HTML Content](actions/create-pdf-from-html-content.md) | POST | Creates a PDF in DocRaptor from HTML content. |
| [Create PDF from URL](actions/create-pdf-from-url.md) | POST | Creates a PDF in DocRaptor from a URL. |

### Xlsx Document

| Action | Method | Description |
| --- | --- | --- |
| [Create XLSX from HTML Content](actions/create-xlsx-from-html-content.md) | POST | Creates an XLSX document in DocRaptor from HTML content. |

