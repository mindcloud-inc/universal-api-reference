# MyEmailVerifier: Native API Reference

A consolidated summary of MyEmailVerifier's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://myemailverifier.com/real-time-email-verification
- **API base URL:** `https://client.myemailverifier.com`

## Authentication

### API Key

Provide the MyEmailVerifier API key used in request paths and multipart form fields.

### Credentials

- **API Key:** `apiKey` · required · Required MyEmailVerifier API key from the client API settings page.

[Official authentication documentation](https://myemailverifier.com/real-time-email-verification)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Email](actions/analyze-email.md) | `GET /email-analysis/analyze/:email/{{credentials.apiKey}}` | [docs](https://client.myemailverifier.com/email-analysis/analyze/test@example.com/XIMjcL0QD5S7XQi0) |
| [Get Credits](actions/get-credits.md) | `GET /verifier/getcredits/{{credentials.apiKey}}` | [docs](https://myemailverifier.com/real-time-email-verification) |
| [Get Email Analysis Status](actions/get-email-analysis-status.md) | `GET /email-analysis/status/{{credentials.apiKey}}` | [docs](https://client.myemailverifier.com/email-analysis/status/XIMjcL0QD5S7XQi0) |
| [Get Verification File Info](actions/get-verification-file-info.md) | `GET /verifier/file_info/{{credentials.apiKey}}/:fileId` | [docs](https://myemailverifier.com/real-time-email-verification) |
| [Upload Verification File](actions/upload-verification-file.md) | `POST /verifier/upload_file` | [docs](https://myemailverifier.com/real-time-email-verification) |
| [Verify Email](actions/verify-email.md) | `GET /verifier/validate_single/:email/{{credentials.apiKey}}` | [docs](https://myemailverifier.com/real-time-email-verification) |
