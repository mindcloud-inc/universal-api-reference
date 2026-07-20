# MailerCheck: Native API Reference

A consolidated summary of MailerCheck's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://developers.mailercheck.com/
- **API base URL:** `https://app.mailercheck.com/api`

## Authentication

### API Token

Authenticate with a MailerCheck API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.mailercheck.com/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `X-Version` | `2022-10-01` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Verification List](actions/create-verification-list.md) | `POST /lists` | [docs](https://developers.mailercheck.com/email) |
| [Delete Verification List](actions/delete-verification-list.md) | `DELETE /lists/:id` | [docs](https://developers.mailercheck.com/email) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://developers.mailercheck.com/account) |
| [Get Async Email Result](actions/get-async-email-result.md) | `GET /check/single-async/:verification_id` | [docs](https://developers.mailercheck.com/email) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /credits` | [docs](https://developers.mailercheck.com/account) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://developers.mailercheck.com/account) |
| [Get Verification List](actions/get-verification-list.md) | `GET /lists/:id` | [docs](https://developers.mailercheck.com/email) |
| [Get Verification List Results](actions/get-verification-list-results.md) | `GET /lists/:id/results` | [docs](https://developers.mailercheck.com/email) |
| [List Verification Lists](actions/list-verification-lists.md) | `GET /lists` | [docs](https://developers.mailercheck.com/email) |
| [Start List Verification](actions/start-list-verification.md) | `PUT /lists/:id/verify` | [docs](https://developers.mailercheck.com/email) |
| [Verify Single Email](actions/verify-single-email.md) | `POST /check/single` | [docs](https://developers.mailercheck.com/email) |
| [Verify Single Email Async](actions/verify-single-email-async.md) | `POST /check/single-async` | [docs](https://developers.mailercheck.com/email) |
