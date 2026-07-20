# <img src="https://images.mindcloud.co/apps/icons/images-32_1774902907722.png" alt="fynk logo" width="28" height="28"> fynk: Universal API

Create and manage fynk documents, templates, metadata, signatories, parties, file storage, comments, and document stage transitions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fynk/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 39
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fynk.com
- **Vendor API docs:** https://app.fynk.com/v1/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current API Token Details](actions/get-current-api-token-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-current-api-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (39)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Current API Token Details](actions/get-current-api-token-details.md) | GET | Retrieves the current API token details from fynk. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Comment](actions/get-document-comment.md) | GET | Retrieves a document comment from fynk. |
| [List Document Comments](actions/list-document-comments.md) | GET | Retrieves comments for a document in fynk. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document From PDF](actions/create-document-from-pdf.md) | POST | Creates a new document from a PDF in fynk. |
| [Create Document From Template](actions/create-document-from-template.md) | POST | Creates a new document from a template in fynk. |
| [Download Latest Revision PDF](actions/download-latest-revision-pdf.md) | GET | Retrieves the latest revision PDF from fynk. |
| [Get Document](actions/get-document.md) | GET | Retrieves detailed information for a document from fynk. |
| [Get Latest Revision PDF Details](actions/get-latest-revision-pdf-details.md) | GET | Retrieves the latest revision PDF details from fynk. |
| [List Documents](actions/list-documents.md) | GET | Retrieves a list of documents from fynk. |
| [Move Document To Done Stage](actions/move-document-to-done-stage.md) | PUT | Moves a document to the done stage in fynk. |
| [Move Document To Review Stage](actions/move-document-to-review-stage.md) | PUT | Moves a document to the review stage in fynk. |
| [Move Document To Signing Stage](actions/move-document-to-signing-stage.md) | PUT | Moves a document to the signing stage in fynk. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in fynk. |

### Document File Storage Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Document File Storage Upload URL](actions/create-document-file-storage-upload-url.md) | POST | Creates a document file storage upload URL in fynk. |

### Document Pdf Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Document PDF Upload URL](actions/create-document-pdf-upload-url.md) | POST | Creates a document PDF upload URL in fynk. |

### Dynamic Field

| Action | Method | Description |
| --- | --- | --- |
| [List Document Dynamic Fields](actions/list-document-dynamic-fields.md) | GET | Retrieves dynamic fields for a document in fynk. |
| [Update Document Dynamic Field](actions/update-document-dynamic-field.md) | PUT | Updates a document dynamic field in fynk. |

### Linked Document

| Action | Method | Description |
| --- | --- | --- |
| [Link Documents](actions/link-documents.md) | POST | Creates a linked document relationship in fynk. |
| [List Linked Documents](actions/list-linked-documents.md) | GET | Retrieves linked documents for a document in fynk. |
| [Unlink Documents](actions/unlink-documents.md) | DELETE | Deletes a linked document relationship from fynk. |

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List Metadata](actions/list-metadata.md) | GET | Retrieves available metadata fields from fynk. |

### Metadata Value

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Metadata Value](actions/create-document-metadata-value.md) | POST | Creates a document metadata value in fynk. |
| [Delete Document Metadata Value](actions/delete-document-metadata-value.md) | DELETE | Deletes a document metadata value from fynk. |
| [List Document Metadata Values](actions/list-document-metadata-values.md) | GET | Retrieves metadata values for a document in fynk. |
| [Update Document Metadata Value](actions/update-document-metadata-value.md) | PUT | Updates a document metadata value in fynk. |

### Party

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Party](actions/create-document-party.md) | POST | Creates a document party in fynk. |
| [List Document Parties](actions/list-document-parties.md) | GET | Retrieves parties for a document in fynk. |
| [Update Document Party](actions/update-document-party.md) | PUT | Updates a document party in fynk. |

### Signatory

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Signatory](actions/create-document-signatory.md) | POST | Creates a document signatory in fynk. |
| [Delete Document Signatory](actions/delete-document-signatory.md) | DELETE | Deletes a document signatory from fynk. |
| [List Document Signatories](actions/list-document-signatories.md) | GET | Retrieves signatories for a document in fynk. |
| [Set Signing Order](actions/set-signing-order.md) | PUT | Updates signing order for a document in fynk. |
| [Update Document Signatory](actions/update-document-signatory.md) | PUT | Updates a document signatory in fynk. |

### Stored File

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Stored File](actions/create-document-stored-file.md) | POST | Creates a stored file for a document in fynk. |
| [Get Document Stored File](actions/get-document-stored-file.md) | GET | Retrieves a stored file from fynk. |
| [List Document Stored Files](actions/list-document-stored-files.md) | GET | Retrieves stored files for a document in fynk. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves a list of tags from fynk. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves detailed template information from fynk. |
| [List Templates](actions/list-templates.md) | GET | Retrieves a list of templates from fynk. |

