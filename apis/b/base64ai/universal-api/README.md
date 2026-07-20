# <img src="https://images.mindcloud.co/apps/icons/base64_1782742247021.png" alt="Base64.ai logo" width="28" height="28"> Base64.ai: Universal API

AI-powered document, face, and signature extraction and verification for files and URLs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/base64ai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://base64.ai/
- **Vendor API docs:** https://apidoc.base64.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Asyncscan

| Action | Method | Description |
| --- | --- | --- |
| [Scan Document Asynchronously](actions/scan-document-asynchronously.md) | POST | Starts an asynchronous document scan in Base64.ai. |

### Flow

| Action | Method | Description |
| --- | --- | --- |
| [Create Flow](actions/create-flow.md) | POST | Creates a new flow in Base64.ai. |
| [Delete Flow](actions/delete-flow.md) | DELETE | Deletes an existing flow from Base64.ai. |
| [List Flows](actions/list-flows.md) | GET | Retrieves all flows from Base64.ai. |
| [Update Flow](actions/update-flow.md) | PUT | Updates an existing flow in Base64.ai. |

### Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Result](actions/get-result.md) | GET | Retrieves a specific result from Base64.ai. |
| [Get Result Review Status](actions/get-result-review-status.md) | GET | Retrieves a result and review status from Base64.ai. |
| [List Flow Results](actions/list-flow-results.md) | GET | Retrieves results from a specific Base64.ai flow. |

### Resultquestion

| Action | Method | Description |
| --- | --- | --- |
| [Ask Result Question](actions/ask-result-question.md) | GET | Retrieves answers to questions about a Base64.ai result. |

### Scanresult

| Action | Method | Description |
| --- | --- | --- |
| [Get Asynchronous Scan Result](actions/get-asynchronous-scan-result.md) | GET | Retrieves an asynchronous scan result from Base64.ai. |
| [Mock Document Extraction](actions/mock-document-extraction.md) | POST | Creates a mock extraction result in Base64.ai. |
| [OCR Document by URL](actions/ocr-document-by-url.md) | POST | Creates an OCR result in Base64.ai from a document URL. |
| [Scan Document by URL](actions/scan-document-by-url.md) | POST | Creates a document scan result in Base64.ai from a URL. |
| [Scan Document into Flow](actions/scan-document-into-flow.md) | POST | Creates a document scan result in a Base64.ai flow. |
| [Scan Document Under Page Count](actions/scan-document-under-page-count.md) | POST | Creates a Base64.ai scan result for documents under a page limit. |
| [Scan Document Until Page Number](actions/scan-document-until-page-number.md) | POST | Creates a Base64.ai scan result up to a specified page number. |
| [Scan Document with Document Types](actions/scan-document-with-document-types.md) | POST | Creates a Base64.ai scan result using specified document types. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves user account details from Base64.ai. |

