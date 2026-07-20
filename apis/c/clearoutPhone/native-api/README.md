# ClearoutPhone: Native API Reference

A consolidated summary of ClearoutPhone's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.clearoutphone.io/
- **API base URL:** `https://api.clearoutphone.io/v1`

## Authentication

### API Key (Implicit)

Use a ClearoutPhone API token generated from Dashboard > API to authorize requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.clearoutphone.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Phone Number Validation](actions/create-bulk-phone-number-validation.md) | `POST /phonenumber/bulk` | [docs](https://docs.clearoutphone.io/#api-Phone_Number_Validation_API-BulkPhoneValidate) |
| [Download Bulk Phone Number Validation Result](actions/download-bulk-phone-number-validation-result.md) | `POST /download/result` | [docs](https://docs.clearoutphone.io/#api-Phone_Number_Validation_API-Result) |
| [Get Available Credits](actions/get-available-credits.md) | `GET /phonenumber/getcredits` | [docs](https://docs.clearoutphone.io/#api-Phone_Number_Validation_API-GetCredits) |
| [Get Bulk Phone Number Validation Progress Status](actions/get-bulk-phone-number-validation-progress-status.md) | `GET /phonenumber/bulk/progress_status` | [docs](https://docs.clearoutphone.io/#api-Phone_Number_Validation_API-ProgressStatus) |
| [Validate Phone Number Instantly](actions/validate-phone-number-instantly.md) | `POST /phonenumber/validate` | [docs](https://docs.clearoutphone.io/#api-Phone_Number_Validation_API-InstantPhoneNumberValidation) |
