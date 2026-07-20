# Stiply: Native API Reference

A consolidated summary of Stiply's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://app.stiply.nl/api-documentation/v2
- **OpenAPI specification:** https://app.stiply.nl/v2/.metadata/stiply.json
- **API base URL:** `https://api.stiply.nl`

## Authentication

### Personal Access Token

Authenticate with a Stiply Personal Access Token generated from API settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.stiply.nl/settings/api/tokens)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$page_size` in the query string to set the page size (default 100; accepted range 1–100). Use `$page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Sign Request](actions/cancel-sign-request.md) | `POST /v2/sign_requests/:sign_request/actions/cancel` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/CancelSignRequest) |
| [Delete Sign Request](actions/delete-sign-request.md) | `DELETE /v2/sign_requests/:sign_request` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DeleteSignRequest) |
| [Download Proof Document](actions/download-proof-document.md) | `GET /v2/sign_requests/:sign_request/actions/download_proof_document` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadProofDocument) |
| [Download Sign Request Document](actions/download-sign-request-document.md) | `GET /v2/sign_requests/:sign_request/documents/:document/actions/download_file` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadDocumentFile) |
| [Download Sign Request Files](actions/download-sign-request-files.md) | `GET /v2/sign_requests/:sign_request/actions/download_files` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadSignRequestFiles) |
| [Download Signer Attachment](actions/download-signer-attachment.md) | `GET /v2/sign_requests/:sign_request/signer_attachments/:signer_attachment/actions/download_file` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadSignerAttachment) |
| [Download Signer Attachments](actions/download-signer-attachments.md) | `GET /v2/sign_requests/:sign_request/signers/:signer/actions/download_signer_attachments` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/DownloadSignerAttachments) |
| [Extend Sign Request Term](actions/extend-sign-request-term.md) | `POST /v2/sign_requests/:sign_request/actions/extend_term` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/ExtendSignRequestTerm) |
| [Get Sign Request](actions/get-sign-request.md) | `GET /v2/sign_requests/:sign_request` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequest) |
| [Get Sign Request by External Key](actions/get-sign-request-by-external-key.md) | `GET /v2/sign_requests/by_key/:external_key` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestByExternalKey) |
| [Get Sign Request by Key](actions/get-sign-request-by-key.md) | `GET /v2/sign_requests/by_key/:sign_request_key` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestByKey) |
| [Get Sign Request Signer](actions/get-sign-request-signer.md) | `GET /v2/sign_requests/:sign_request/signers/:signer` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSigner) |
| [Get Signer Attachment](actions/get-signer-attachment.md) | `GET /v2/sign_requests/:sign_request/signer_attachments/:signer_attachment` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSignerAttachment) |
| [List Sign Request Documents](actions/list-sign-request-documents.md) | `GET /v2/sign_requests/:sign_request/documents` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestDocuments) |
| [List Sign Request Progress](actions/list-sign-request-progress.md) | `GET /v2/sign_requests/:sign_request/progress` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestProgress) |
| [List Sign Request Signers](actions/list-sign-request-signers.md) | `GET /v2/sign_requests/:sign_request/signers` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSigners) |
| [List Sign Requests](actions/list-sign-requests.md) | `GET /v2/sign_requests` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequests) |
| [List Signer Attachments](actions/list-signer-attachments.md) | `GET /v2/sign_requests/:sign_request/signer_attachments` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/GetSignRequestSignerAttachments) |
| [Send Sign Request](actions/send-sign-request.md) | `POST /v2/sign_requests` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/SendSignRequest) |
| [Send Sign Request Reminder](actions/send-sign-request-reminder.md) | `POST /v2/sign_requests/:sign_request/actions/send_reminder` | [docs](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/SendSignRequestReminder) |
