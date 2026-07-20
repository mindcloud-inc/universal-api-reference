# SMSup: Native API Reference

A consolidated summary of SMSup's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://app.smsup.es/api/3.0/docs/
- **API base URL:** `https://api.gateway360.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.smsup.es/api/3.0/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Subaccount Balance](actions/add-subaccount-balance.md) | `POST /api/3.0/subaccount/add-balance` | [docs](https://app.smsup.es/api/3.0/docs/subaccount/add-balance) |
| [Create Subaccount](actions/create-subaccount.md) | `POST /api/3.0/subaccount/create` | [docs](https://app.smsup.es/api/3.0/docs/subaccount/create) |
| [Deduct Subaccount Balance](actions/deduct-subaccount-balance.md) | `POST /api/3.0/subaccount/deduct-balance` | [docs](https://app.smsup.es/api/3.0/docs/subaccount/deduct-balance) |
| [Delete Subaccount](actions/delete-subaccount.md) | `POST /api/3.0/subaccount/delete` | [docs](https://app.smsup.es/api/3.0/docs/subaccount/delete) |
| [Get Account Balance](actions/get-account-balance.md) | `POST /api/3.0/account/get-balance` | [docs](https://app.smsup.es/api/3.0/docs/account/get-balance) |
| [Get Country Pricing](actions/get-country-pricing.md) | `POST /api/3.0/account/pricing/sms/get-country-pricing` | [docs](https://app.smsup.es/api/3.0/docs/account/get-pricing) |
| [Get Prefix Pricing](actions/get-prefix-pricing.md) | `POST /api/3.0/account/pricing/sms/get-prefix-pricing` | [docs](https://app.smsup.es/api/3.0/docs/account/get-pricing) |
| [Get Subaccount Balance](actions/get-subaccount-balance.md) | `POST /api/3.0/subaccount/get-balance` | [docs](https://app.smsup.es/api/3.0/docs/subaccount/get-balance) |
| [Get Subaccount Info](actions/get-subaccount-info.md) | `POST /api/3.0/subaccount/get-info` | [docs](https://app.smsup.es/api/3.0/docs/subaccount/get-info) |
| [Request HLR Lookup](actions/request-hlr-lookup.md) | `POST /api/hlr/request` | [docs](https://app.smsup.es/api/3.0/docs/hlr/lookup) |
| [Request PIN](actions/request-pin.md) | `POST /api/2fa/request` | [docs](https://app.smsup.es/api/3.0/docs/2factor/request) |
| [Send SMS](actions/send-sms.md) | `POST /api/3.0/sms/send` | [docs](https://app.smsup.es/api/3.0/docs/sms/send) |
| [Send SMS Landing](actions/send-sms-landing.md) | `POST /api/3.0/sms/send-landing` | [docs](https://app.smsup.es/api/3.0/docs/landing/send) |
| [Send SMS Link](actions/send-sms-link.md) | `POST /api/3.0/sms/send-link` | [docs](https://app.smsup.es/api/3.0/docs/link/send) |
| [Send SMS Survey](actions/send-sms-survey.md) | `POST /api/3.0/sms/send-survey` | [docs](https://app.smsup.es/api/3.0/docs/survey/send) |
| [Verify PIN](actions/verify-pin.md) | `POST /api/2fa/verify` | [docs](https://app.smsup.es/api/3.0/docs/2factor/verify) |
