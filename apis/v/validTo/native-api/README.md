# validTo: Native API Reference

A consolidated summary of validTo's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://validto.readme.io/reference/overview
- **API base URL:** `https://api.validto.com/v1`

## Authentication

### API Key

Use your validTo API key to access the email validation API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://validto.readme.io/reference/authentication)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Validation List](actions/create-bulk-validation-list.md) | `POST /bulk` | [docs](https://validto.readme.io/reference/create-a-bulk-validation-list) |
| [Delete Bulk Validation List](actions/delete-bulk-validation-list.md) | `DELETE /bulk/:jobId` | [docs](https://validto.readme.io/reference/delete-a-bulk-validation-list) |
| [Download Bulk Validation Results](actions/download-bulk-validation-results.md) | `POST /download` | [docs](https://validto.readme.io/reference/download-a-bulk-validation-list) |
| [Get Bulk Validation Progress](actions/get-bulk-validation-progress.md) | `GET /bulk/:jobId` | [docs](https://validto.readme.io/reference/progress-of-a-bulk-validation-list) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /info` | [docs](https://validto.readme.io/reference/get-credit-balance) |
| [Start Bulk Validation](actions/start-bulk-validation.md) | `PATCH /bulk/:jobId` | [docs](https://validto.readme.io/reference/verify-a-bulk-validation-list) |
| [Verify Email Address](actions/verify-email-address.md) | `GET /verify` | [docs](https://validto.readme.io/reference/single-validation-api) |
