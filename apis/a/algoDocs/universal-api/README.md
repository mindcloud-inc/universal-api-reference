# <img src="https://images.mindcloud.co/apps/icons/idvq-cci-naf-logos_1774893528732.png" alt="AlgoDocs logo" width="28" height="28"> AlgoDocs: Universal API

Automate document extraction, classification, and review workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/algoDocs/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://algodocs.com
- **Vendor API docs:** https://api.algodocs.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algoDocs/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Upload Document From Local Path](actions/upload-document-from-local-path.md) | POST | Creates a document in AlgoDocs from a local file. |
| [Upload Document From URL](actions/upload-document-from-url.md) | POST | Creates a document in AlgoDocs from a public URL. |
| [Upload Document With Base64](actions/upload-document-with-base64.md) | POST | Creates a document in AlgoDocs from base64 content. |

### Extracted Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Extracted Data of a Single Document](actions/get-extracted-data-of-a-single-document.md) | GET | Retrieves extracted data from one AlgoDocs document. |
| [Get Extracted Data of Multiple Documents](actions/get-extracted-data-of-multiple-documents.md) | GET | Retrieves extracted data from AlgoDocs documents by extractor. |

### Extractor

| Action | Method | Description |
| --- | --- | --- |
| [List Document Data Extractors](actions/list-document-data-extractors.md) | GET | Retrieves document data extractors from AlgoDocs. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from your AlgoDocs account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current AlgoDocs user. |

