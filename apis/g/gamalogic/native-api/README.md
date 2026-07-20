# Gamalogic: Native API Reference

A consolidated summary of Gamalogic's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.gamalogic.com/documentation/introduction
- **API base URL:** `https://gamalogic.com`

## Authentication

### API Key

Authenticate requests with a Gamalogic API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.gamalogic.com/documentation/introduction)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Batch Result](actions/download-batch-result.md) | `GET /batchresult` | [docs](https://docs.gamalogic.com/emails/download-batch) |
| [Find Email](actions/find-email.md) | `GET /email-discovery` | [docs](https://docs.gamalogic.com/find-email/single-email-finder) |
| [Get Batch Status](actions/get-batch-status.md) | `GET /batchstatus` | [docs](https://docs.gamalogic.com/emails/status-batch) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /creditbalance` | [docs](https://docs.gamalogic.com/balance-credit) |
| [Verify Batch Emails](actions/verify-batch-emails.md) | `POST /batchemailvrf` | [docs](https://docs.gamalogic.com/emails/verify-batch) |
| [Verify Email](actions/verify-email.md) | `GET /emailvrf` | [docs](https://docs.gamalogic.com/emails/verify-email) |
