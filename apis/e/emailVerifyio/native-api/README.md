# EmailVerify.io: Native API Reference

A consolidated summary of EmailVerify.io's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://www.emailverify.io/api/docs/
- **API base URL:** `https://app.emailverify.io/api/v1`

## Authentication

### EmailVerify.io API Key

Use your EmailVerify.io API key. This app is configured for the documented provider contract where GET routes send the key in the query string and the bulk POST route sends it in the JSON body.

### Credentials

- **API Key:** `apiKey` · required · Your EmailVerify.io API key.

[Official authentication documentation](https://www.emailverify.io/api/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Account Balance](actions/check-account-balance.md) | `GET /check-account-balance/` | [docs](https://www.emailverify.io/api/docs/#verifier) |
| [Find Business Email](actions/find-business-email.md) | `GET /finder` | [docs](https://www.emailverify.io/api/docs/#finder) |
| [Get Bulk Verification Result](actions/get-bulk-verification-result.md) | `GET /get-result-bulk-verification-task/` | [docs](https://www.emailverify.io/api/docs/#bulk) |
| [Start Bulk Verification Task](actions/start-bulk-verification-task.md) | `POST /validate-batch` | [docs](https://www.emailverify.io/api/docs/#bulk) |
| [Validate Email](actions/validate-email.md) | `GET /validate` | [docs](https://www.emailverify.io/api/docs/#verifier) |
