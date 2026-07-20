# QuickEmailVerification: Native API Reference

A consolidated summary of QuickEmailVerification's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.quickemailverification.com/email-verification-api/kick-start-with-email-validation-api
- **API base URL:** `https://api.quickemailverification.com/v1`

## Authentication

### API Key

Connect QuickEmailVerification with an API key generated from API Settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.quickemailverification.com/email-verification-api/kick-start-with-email-validation-api)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | `GET /verify` | [docs](https://docs.quickemailverification.com/email-verification-api/verify-an-email-address) |
| [Verify Email in Sandbox Mode](actions/verify-email-in-sandbox-mode.md) | `GET /verify/sandbox` | [docs](https://docs.quickemailverification.com/email-verification-api/sandbox-mode) |
