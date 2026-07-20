# Nvoip: Native API Reference

A consolidated summary of Nvoip's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://nvoip.docs.apiary.io/
- **API base URL:** `https://api.nvoip.com.br/v2`

## Authentication

### Access Token

Use a Nvoip access token as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://suporte.nvoip.com.br/portal/pt/kb/articles/napikey-user-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check OTP](actions/check-otp.md) | `GET /check/otp` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/otp.html) |
| [Check 2FA Code](actions/check2fa-code.md) | `GET /check/2fa` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/2fa.html) |
| [Create Call](actions/create-call.md) | `POST /calls/` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/calls.html) |
| [Delete Scheduled SMS](actions/delete-scheduled-sms.md) | `DELETE /delete/sched/torpedo` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js) |
| [End Call](actions/end-call.md) | `GET /endcall` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/calls.html) |
| [Generate Access Token](actions/generate-access-token.md) | `POST /oauth/token` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js) |
| [Get Balance](actions/get-balance.md) | `GET /balance` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js) |
| [List Scheduled SMS](actions/list-scheduled-sms.md) | `GET /list/sched/torpedo` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js) |
| [Schedule SMS](actions/schedule-sms.md) | `POST /sched/torpedo` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/index.js) |
| [Send OTP](actions/send-otp.md) | `POST /otp` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/otp.html) |
| [Send Voice Blast](actions/send-voice-blast.md) | `POST /torpedo/voice` | [docs](https://github.com/Nvoip/nvoip-integrationAPI/blob/main/torpedo.html) |
