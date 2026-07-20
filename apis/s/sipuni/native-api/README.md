# Sipuni: Native API Reference

A consolidated summary of Sipuni's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://doc.sipuni.com/articles/636--api/
- **API base URL:** `https://sipuni.com/api`

## Authentication

### Sipuni Custom Auth

Use the Sipuni account ID and integration key to sign statistics requests.

### Credentials

- **Account ID:** `accountId` · required · Sipuni account ID used as the `user` request field.
- **Integration Key:** `integrationKey` · required · Sipuni integration key used to compute the request hash.

[Official authentication documentation](https://doc.sipuni.com/articles/636-643--generaciya-klyucha-integracii/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

Responses from this API use plain text.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Call Number](actions/call-number.md) | `POST /callback/call_number` | [docs](https://doc.sipuni.com/articles/636-640--otpravka-sobytij-http/) |
| [Export All Statistics](actions/export-all-statistics.md) | `GET /statistic/export/all` | [docs](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/) |
| [Export Statistics](actions/export-statistics.md) | `GET /statistic/export` | [docs](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/) |
| [Get CRM Recording](actions/get-crm-recording.md) | `GET /crm/record` | [docs](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/) |
| [Get Recording](actions/get-recording.md) | `GET /statistic/record` | [docs](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/) |
| [List Operators](actions/list-operators.md) | `GET /statistic/operators` | [docs](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/) |
