# <img src="https://images.mindcloud.co/apps/icons/favicon-docs-docutray-com-48x48_1776089082903.png" alt="Docutray logo" width="28" height="28"> Docutray: Universal API

Convert, identify, and manage documents and knowledge bases

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docutray/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://docutray.com
- **Vendor API docs:** https://docs.docutray.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Document Types](actions/list-document-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-document-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Start Document Conversion](actions/convert-document-async.md) | POST |  |

### Conversion Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversion Status](actions/get-conversion-status.md) | GET |  |

### Converted Document

| Action | Method | Description |
| --- | --- | --- |
| [Convert Document](actions/convert-document.md) | POST |  |

### Document Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Type](actions/create-document-type.md) | POST |  |
| [Get Document Type](actions/get-document-type.md) | GET |  |
| [List Document Types](actions/list-document-types.md) | GET |  |
| [Update Document Type](actions/update-document-type.md) | PUT |  |

### Document Type Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Document Type](actions/validate-document.md) | GET |  |

### Identification

| Action | Method | Description |
| --- | --- | --- |
| [Start Document Identification](actions/identify-document-async.md) | POST |  |

### Identification Result

| Action | Method | Description |
| --- | --- | --- |
| [Identify Document](actions/identify-document.md) | POST |  |

### Identification Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Identification Status](actions/get-identification-status.md) | GET |  |

### Knowledge Base

| Action | Method | Description |
| --- | --- | --- |
| [Create Knowledge Base](actions/create-knowledge-base.md) | POST |  |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | DELETE |  |
| [Get Knowledge Base](actions/get-knowledge-base.md) | GET |  |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | GET |  |
| [Update Knowledge Base](actions/update-knowledge-base.md) | PUT |  |

### Knowledge Base Document

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Upload Knowledge Base Documents](actions/bulk-upload-knowledge-base-documents.md) | POST |  |
| [Delete Knowledge Base Document](actions/delete-knowledge-base-document.md) | DELETE |  |
| [Get Knowledge Base Document](actions/get-knowledge-base-document.md) | GET |  |
| [List Knowledge Base Documents](actions/list-knowledge-base-documents.md) | GET |  |
| [Update Knowledge Base Document](actions/update-knowledge-base-document.md) | PUT |  |
| [Upload Knowledge Base Document](actions/upload-knowledge-base-document.md) | POST |  |

### Knowledge Base Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Advanced Search Knowledge Base](actions/search-knowledge-base.md) | GET |  |
| [Search Knowledge Base](actions/search-knowledge-base-get.md) | GET |  |

### Knowledge Base Sync

| Action | Method | Description |
| --- | --- | --- |
| [Sync Knowledge Base](actions/sync-knowledge-base.md) | POST |  |

### Step Execution

| Action | Method | Description |
| --- | --- | --- |
| [Start Step Execution](actions/execute-step-async.md) | POST |  |

### Step Execution Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Step Execution Status](actions/get-step-execution-status.md) | GET |  |

