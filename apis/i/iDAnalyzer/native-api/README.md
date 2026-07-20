# ID Analyzer: Native API Reference

A consolidated summary of ID Analyzer's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://developer.idanalyzer.com/
- **API base URL:** `https://api2.idanalyzer.com`

## Authentication

### Server API Key

Authenticate with the ID Analyzer Server API Key. MindCloud injects the key into the X-API-KEY request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developer.idanalyzer.com/docs/authentication-type)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create a document template](actions/create-a-document-template.md) | `POST /contract` | [docs](https://developer.idanalyzer.com/reference/post-contract-2) |
| [Create a hosted Docupass flow](actions/create-a-hosted-docupass-flow.md) | `POST /docupass` | [docs](https://developer.idanalyzer.com/reference/post-docupass) |
| [Delete a document template](actions/delete-a-document-template.md) | `DELETE /contract/:templateId` | [docs](https://developer.idanalyzer.com/reference/delete-contract-templateid-2) |
| [Delete a Docupass session](actions/delete-a-docupass-session.md) | `DELETE /docupass/:reference` | [docs](https://developer.idanalyzer.com/reference/delete-docupass-reference-2) |
| [Delete a saved transaction](actions/delete-a-saved-transaction.md) | `DELETE /transaction/:transactionId` | [docs](https://developer.idanalyzer.com/reference/delete-transaction-transactionid) |
| [Export saved transactions](actions/export-saved-transactions.md) | `POST /export/transaction` | [docs](https://developer.idanalyzer.com/reference/post-export-transaction-2) |
| [Generate a document from a template](actions/generate-a-document-from-a-template.md) | `POST /generate` | [docs](https://developer.idanalyzer.com/reference/post-generate-1) |
| [Get a document template](actions/get-a-document-template.md) | `GET /contract/:templateId` | [docs](https://developer.idanalyzer.com/reference/get-contract-templateid-2) |
| [Get a Docupass session](actions/get-a-docupass-session.md) | `GET /docupass/:reference` | [docs](https://developer.idanalyzer.com/reference/get-docupass-reference) |
| [Get a saved transaction](actions/get-a-saved-transaction.md) | `GET /transaction/:transactionId` | [docs](https://developer.idanalyzer.com/reference/get-transaction-transactionid) |
| [Get a KYC profile](actions/get-akyc-profile.md) | `GET /profile/:profileId` | [docs](https://developer.idanalyzer.com/reference/get-profile-profileid-2) |
| [List document templates](actions/list-document-templates.md) | `GET /contract` | [docs](https://developer.idanalyzer.com/reference/get-contract-1) |
| [List Docupass sessions](actions/list-docupass-sessions.md) | `GET /docupass` | [docs](https://developer.idanalyzer.com/reference/get-docupass-2) |
| [List KYC Profiles](actions/list-kyc-profiles.md) | `GET /profile` | [docs](https://developer.idanalyzer.com/reference/get-profile-2) |
| [List saved transactions](actions/list-saved-transactions.md) | `GET /transaction` | [docs](https://developer.idanalyzer.com/reference/get-transaction-3) |
| [Run a fast OCR document scan](actions/run-a-fast-ocr-document-scan.md) | `POST /quickscan` | [docs](https://developer.idanalyzer.com/reference/post-quickscan-2) |
| [Run a full ID verification scan](actions/run-a-full-id-verification-scan.md) | `POST /scan` | [docs](https://developer.idanalyzer.com/reference/post-scan) |
| [Update a document template](actions/update-a-document-template.md) | `POST /contract/:templateId` | [docs](https://developer.idanalyzer.com/reference/post-contract-templateid-2) |
| [Update the final transaction decision](actions/update-the-final-transaction-decision.md) | `PATCH /transaction/:transactionId` | [docs](https://developer.idanalyzer.com/reference/patch-transaction-transactionid) |
