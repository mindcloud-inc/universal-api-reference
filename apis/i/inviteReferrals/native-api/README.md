# InviteReferrals: Native API Reference

A consolidated summary of InviteReferrals's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.invitereferrals.com/
- **API base URL:** `https://www.ref-r.com/api/v1`

## Authentication

### Brand Credentials

InviteReferrals REST credentials using brand ID and secret key, with optional encrypted key for related SSO flows.

### Credentials

- **Secret Key:** `apiKey` · required · Secret key used for InviteReferrals REST API authentication.
- **Brand ID:** `brandId` · required · InviteReferrals brand identifier sent alongside API requests.
- **Encrypted Key:** `encryptedKey` · optional · Encrypted key used by InviteReferrals SSO and JavaScript widget flows when needed.

Send these headers with each API request:

```http
x-api-key: <apiKey>
x-brand-id: <brandId>
```

[Official authentication documentation](https://docs.invitereferrals.com/docs/single-sign-on)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Conversion](actions/add-conversion.md) | `POST /conversion/add` | [docs](https://docs.invitereferrals.com/reference/add-conversion) |
| [Approve Or Reject Conversion](actions/approve-or-reject-conversion.md) | `POST /conversion/confirm` | [docs](https://docs.invitereferrals.com/reference/approvereject-conversion) |
