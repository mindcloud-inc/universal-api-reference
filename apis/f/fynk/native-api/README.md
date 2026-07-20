# fynk: Native API Reference

A consolidated summary of fynk's API configuration and 39 documented operations, with links to official documentation.

- **Official docs:** https://app.fynk.com/v1/docs
- **OpenAPI specification:** https://app.fynk.com/v1/docs/openapi.json
- **API base URL:** `https://app.fynk.com/v1/api`

## Authentication

### API Token

Authenticate fynk requests with a bearer API token. Paste the fynk API token into the MindCloud API Key field. MindCloud adds the Authorization bearer header automatically for this auth type.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.fynk.com/en/articles/418748-rest-api-reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (39 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document File Storage Upload URL](actions/create-document-file-storage-upload-url.md) | `POST /file-uploads/document-file-storage` | [docs](https://app.fynk.com/v1/docs#/operations/v1.file-uploads.document-file-storage.create) |
| [Create Document From PDF](actions/create-document-from-pdf.md) | `POST /documents/create-from-pdf` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.create-from-pdf) |
| [Create Document From Template](actions/create-document-from-template.md) | `POST /documents/create-from-template` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.create-from-template) |
| [Create Document Metadata Value](actions/create-document-metadata-value.md) | `POST /documents/:document/metadata-values` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.metadata-values.store) |
| [Create Document Party](actions/create-document-party.md) | `POST /documents/:document/parties` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.parties.store) |
| [Create Document PDF Upload URL](actions/create-document-pdf-upload-url.md) | `POST /file-uploads/document-pdf` | [docs](https://app.fynk.com/v1/docs#/operations/v1.file-uploads.document-pdf.create) |
| [Create Document Signatory](actions/create-document-signatory.md) | `POST /documents/:document/signatories` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.store) |
| [Create Document Stored File](actions/create-document-stored-file.md) | `POST /documents/:document/file-storage` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.document-file-storage.store) |
| [Delete Document Metadata Value](actions/delete-document-metadata-value.md) | `DELETE /documents/:document/metadata-values/:metadataValue` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.metadata-values.destroy) |
| [Delete Document Signatory](actions/delete-document-signatory.md) | `DELETE /documents/:document/signatories/:signatory` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.destroy) |
| [Download Latest Revision PDF](actions/download-latest-revision-pdf.md) | `GET /documents/:document/revisions/latest/pdf/download` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.revisions.latest.pdf.download) |
| [Get Current API Token Details](actions/get-current-api-token-details.md) | `GET /me` | [docs](https://app.fynk.com/v1/docs#/operations/v1.api-tokens.show-me) |
| [Get Document](actions/get-document.md) | `GET /documents/:document` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.show) |
| [Get Document Comment](actions/get-document-comment.md) | `GET /documents/:document/comments/:comment` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.comments.show) |
| [Get Document Stored File](actions/get-document-stored-file.md) | `GET /documents/:document/file-storage/:storedFile` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.document-file-storage.show) |
| [Get Latest Revision PDF Details](actions/get-latest-revision-pdf-details.md) | `GET /documents/:document/revisions/latest/pdf` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.revisions.latest.pdf.show) |
| [Get Template](actions/get-template.md) | `GET /templates/:template` | [docs](https://app.fynk.com/v1/docs#/operations/v1.templates.show) |
| [Link Documents](actions/link-documents.md) | `POST /documents/:document/linked-documents` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.linked-documents.store) |
| [List Document Comments](actions/list-document-comments.md) | `GET /documents/:document/comments` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.comments.index) |
| [List Document Dynamic Fields](actions/list-document-dynamic-fields.md) | `GET /documents/:document/dynamic-fields` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.dynamic-fields.index) |
| [List Document Metadata Values](actions/list-document-metadata-values.md) | `GET /documents/:document/metadata-values` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.metadata-values.index) |
| [List Document Parties](actions/list-document-parties.md) | `GET /documents/:document/parties` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.parties.index) |
| [List Document Signatories](actions/list-document-signatories.md) | `GET /documents/:document/signatories` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.index) |
| [List Document Stored Files](actions/list-document-stored-files.md) | `GET /documents/:document/file-storage` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.document-file-storage.index) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.index) |
| [List Linked Documents](actions/list-linked-documents.md) | `GET /documents/:document/linked-documents` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.linked-documents.index) |
| [List Metadata](actions/list-metadata.md) | `GET /metadata` | [docs](https://app.fynk.com/v1/docs#/operations/v1.metadata.index) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://app.fynk.com/v1/docs#/operations/v1.tags.index) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://app.fynk.com/v1/docs#/operations/v1.templates.index) |
| [Move Document To Done Stage](actions/move-document-to-done-stage.md) | `POST /documents/:document/stage-transitions/done` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.stage-transitions.done) |
| [Move Document To Review Stage](actions/move-document-to-review-stage.md) | `POST /documents/:document/stage-transitions/review` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.stage-transitions.review) |
| [Move Document To Signing Stage](actions/move-document-to-signing-stage.md) | `POST /documents/:document/stage-transitions/signing` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.stage-transitions.signing) |
| [Set Signing Order](actions/set-signing-order.md) | `PUT /documents/:document/signatories/order` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.order) |
| [Unlink Documents](actions/unlink-documents.md) | `DELETE /documents/:document/linked-documents/:documentRelationship` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.linked-documents.destroy) |
| [Update Document](actions/update-document.md) | `PUT /documents/:document` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.update) |
| [Update Document Dynamic Field](actions/update-document-dynamic-field.md) | `PUT /documents/:document/dynamic-fields/:dynamicField` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.dynamic-fields.update) |
| [Update Document Metadata Value](actions/update-document-metadata-value.md) | `PUT /documents/:document/metadata-values/:metadataValue` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.metadata-values.update) |
| [Update Document Party](actions/update-document-party.md) | `PUT /documents/:document/parties/:party` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.parties.update) |
| [Update Document Signatory](actions/update-document-signatory.md) | `PUT /documents/:document/signatories/:signatory` | [docs](https://app.fynk.com/v1/docs#/operations/v1.documents.signatories.update) |
