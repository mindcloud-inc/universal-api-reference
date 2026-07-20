# Novofon: Native API Reference

A consolidated summary of Novofon's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://novofon.com/instructions/api/
- **API base URL:** `https://api.novofon.com`

## Authentication

### API Key

Novofon legacy REST API authentication using a key, companion secret, and request-specific signature header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://novofon.com/instructions/api/#direct_numbers_number)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | `GET /v1/info/balance/` | [docs](https://novofon.com/instructions/api/#balance) |
| [Get Call Statistics](actions/get-call-statistics.md) | `GET /v1/statistics/` | [docs](https://novofon.com/instructions/api/#statistics) |
| [Get Callback Widget Statistics](actions/get-callback-widget-statistics.md) | `GET /v1/statistics/callback_widget/` | [docs](https://novofon.com/instructions/api/#statistics_callback_widget) |
| [Get Direct Number](actions/get-direct-number.md) | `GET /v1/direct_numbers/number/` | [docs](https://novofon.com/instructions/api/#direct_numbers_number) |
| [Get Incoming Call Statistics](actions/get-incoming-call-statistics.md) | `GET /v1/statistics/incoming-calls/` | [docs](https://novofon.com/instructions/api/#statistics_incoming) |
| [Get PBX Call Statistics](actions/get-pbx-call-statistics.md) | `GET /v1/statistics/pbx/` | [docs](https://novofon.com/instructions/api/#statistics_pbx) |
| [Get PBX Internal Status](actions/get-pbx-internal-status.md) | `GET /v1/pbx/internal/:pbxSip/status/` | [docs](https://novofon.com/instructions/api/#pbx_internal_status) |
| [Get SIP Status](actions/get-sip-status.md) | `GET /v1/sip/:sipId/status/` | [docs](https://novofon.com/instructions/api/#sip_status) |
| [Get Timezone](actions/get-timezone.md) | `GET /v1/info/timezone/` | [docs](https://novofon.com/instructions/api/#timezone) |
| [List Currencies](actions/list-currencies.md) | `GET /v1/info/lists/currencies/` | [docs](https://novofon.com/instructions/api/#currencies) |
| [List Direct Number Countries](actions/list-direct-number-countries.md) | `GET /v1/direct_numbers/countries/` | [docs](https://novofon.com/instructions/api/#direct_numbers_countries) |
| [List Direct Numbers](actions/list-direct-numbers.md) | `GET /v1/direct_numbers/` | [docs](https://novofon.com/instructions/api/#direct_numbers) |
| [List Languages](actions/list-languages.md) | `GET /v1/info/lists/languages/` | [docs](https://novofon.com/instructions/api/#languages) |
| [List PBX Internal Numbers](actions/list-pbx-internal-numbers.md) | `GET /v1/pbx/internal/` | [docs](https://novofon.com/instructions/api/#pbx_internal) |
| [List SIP Numbers](actions/list-sip-numbers.md) | `GET /v1/sip/` | [docs](https://novofon.com/instructions/api/#sip) |
| [Request Call Recording](actions/request-call-recording.md) | `GET /v1/pbx/record/request/` | [docs](https://novofon.com/instructions/api/#record) |
| [Request Callback](actions/request-callback.md) | `GET /v1/request/callback/` | [docs](https://novofon.com/instructions/api/#callback) |
| [Request Check Number](actions/request-check-number.md) | `GET /v1/request/checknumber/` | [docs](https://novofon.com/instructions/api/#checknumber) |
