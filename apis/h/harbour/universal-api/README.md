# <img src="https://images.mindcloud.co/apps/icons/images-20_1774641259746.png" alt="Harbour logo" width="28" height="28"> Harbour: Universal API

Harbour is a document workflow platform for creating, sending, and managing documents and signatures.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/harbour/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.harbourshare.com
- **Vendor API docs:** https://developers.harbourshare.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Convert Document](actions/convert-document.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agreement Link Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Agreement Link Submission](actions/get-agreement-link-submission.md) | GET | Retrieves a specific agreement link submission from Harbour. |
| [List Agreement Link Submissions](actions/list-agreement-link-submissions.md) | GET | Retrieves submissions for an agreement link from Harbour. |

### Agreement Links

| Action | Method | Description |
| --- | --- | --- |
| [Create Agreement Link](actions/create-agreement-link.md) | POST | Creates a new agreement link in Harbour. |
| [Download Agreement Link](actions/download-agreement-link.md) | GET | Retrieves downloadable agreement link files from Harbour. |
| [Get Agreement Link](actions/get-agreement-link.md) | GET | Retrieves a specific agreement link from Harbour. |
| [List Agreement Links](actions/list-agreement-links.md) | GET | Retrieves a list of agreement links from Harbour. |

### Agreements

| Action | Method | Description |
| --- | --- | --- |
| [Create Agreement](actions/create-agreement.md) | POST | Creates a new agreement in Harbour. |
| [Download Agreement](actions/download-agreement.md) | GET | Retrieves downloadable agreement files from Harbour. |
| [Get Agreement](actions/get-agreement.md) | GET | Retrieves a specific agreement from Harbour. |
| [List Agreements](actions/list-agreements.md) | GET | Retrieves a list of agreements from Harbour. |

### Brands

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand](actions/get-brand.md) | GET | Retrieves a specific brand from Harbour. |
| [List Brands](actions/list-brands.md) | GET | Retrieves a list of brands from Harbour. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Annotate Document](actions/annotate-document.md) | PUT | Adds annotations to an existing document in Harbour. |
| [Convert Document](actions/convert-document.md) | GET | Converts a Harbour document and returns a download URL. |
| [Convert Document From Base64](actions/convert-document-from-base64.md) | GET | Converts a base64 document in Harbour and returns a download URL. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Harbour. |
| [Get Document](actions/get-document.md) | GET | Retrieves a specific document from Harbour. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from Harbour. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a specific folder from Harbour. |
| [List Folders](actions/list-folders.md) | GET | Retrieves a list of folders from Harbour. |

### Insights

| Action | Method | Description |
| --- | --- | --- |
| [Create Insights](actions/create-insights.md) | POST | Creates document insights from completed documents, drafts, or URLs in Harbour. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves a specific item from Harbour. |
| [List Items](actions/list-items.md) | GET | Retrieves a list of items from Harbour. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Harbour. |

