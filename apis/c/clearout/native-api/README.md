# Clearout: Native API Reference

A consolidated summary of Clearout's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.clearout.io/developers/api/overview
- **API base URL:** `https://api.clearout.io/v2`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.clearout.io/developers/api/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Bulk Email Finder Batch](actions/cancel-bulk-email-finder-batch.md) | `POST /email_finder/list/cancel` | [docs](https://docs.clearout.io/developers/api/email-finder) |
| [Cancel Bulk Email Verification Batch](actions/cancel-bulk-email-verification-batch.md) | `POST /email_verify/list/cancel` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Create Bulk Email Finder Batch](actions/create-bulk-email-finder-batch.md) | `POST /email_finder/bulk` | [docs](https://docs.clearout.io/developers/api/email-finder) |
| [Create Bulk Email Verification Batch](actions/create-bulk-email-verification-batch.md) | `POST /email_verify/bulk` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Delete Bulk Email Verification Result](actions/delete-bulk-email-verification-result.md) | `POST /email_verify/list/remove` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Download Bulk Email Finder Result](actions/download-bulk-email-finder-result.md) | `POST /email_finder/download/result` | [docs](https://docs.clearout.io/developers/api/email-finder) |
| [Download Bulk Email Verification Result](actions/download-bulk-email-verification-result.md) | `POST /download/result` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Find Email Instantly](actions/find-email-instantly.md) | `POST /email_finder/instant` | [docs](https://docs.clearout.io/developers/api/email-finder) |
| [Find MX Records](actions/find-mx-records.md) | `POST /domain/resolve/mx` | [docs](https://docs.clearout.io/developers/api/misc-domain-api) |
| [Find Whois](actions/find-whois.md) | `POST /domain/resolve/whois` | [docs](https://docs.clearout.io/developers/api/misc-domain-api) |
| [Get Available Credits](actions/get-available-credits.md) | `GET /email_verify/getcredits` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Get Bulk Email Finder Batch Status](actions/get-bulk-email-finder-batch-status.md) | `GET /email_finder/bulk/progress_status` | [docs](https://docs.clearout.io/developers/api/email-finder) |
| [Get Bulk Email Verification Batch Status](actions/get-bulk-email-verification-batch-status.md) | `GET /email_verify/bulk/progress_status` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Get Instant Email Finder Status](actions/get-instant-email-finder-status.md) | `GET /email_finder/instant/queue_status` | [docs](https://docs.clearout.io/developers/api/email-finder) |
| [Remove Bulk Email Finder List](actions/remove-bulk-email-finder-list.md) | `POST /email_finder/list/remove` | [docs](https://docs.clearout.io/developers/api/email-finder) |
| [Reverse Lookup Domain](actions/reverse-lookup-domain.md) | `GET /reverse_lookup/domain` | [docs](https://docs.clearout.io/developers/api/reverse-lookup) |
| [Reverse Lookup Email Address](actions/reverse-lookup-email-address.md) | `GET /reverse_lookup/email` | [docs](https://docs.clearout.io/developers/api/reverse-lookup) |
| [Reverse Lookup LinkedIn Profile](actions/reverse-lookup-linked-in-profile.md) | `GET /reverse_lookup/linkedin` | [docs](https://docs.clearout.io/developers/api/reverse-lookup) |
| [Verify Business Email](actions/verify-business-email.md) | `POST /email/verify/business` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Verify Catch-All Email](actions/verify-catch-all-email.md) | `POST /email/verify/catchall` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Verify Disposable Email](actions/verify-disposable-email.md) | `POST /email/verify/disposable` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Verify Email Instantly](actions/verify-email-instantly.md) | `POST /email_verify/instant` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Verify Free Email](actions/verify-free-email.md) | `POST /email/verify/free` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Verify Gibberish Email](actions/verify-gibberish-email.md) | `POST /email/verify/gibberish` | [docs](https://docs.clearout.io/developers/api/email-verify) |
| [Verify Role Email](actions/verify-role-email.md) | `POST /email/verify/role` | [docs](https://docs.clearout.io/developers/api/email-verify) |
