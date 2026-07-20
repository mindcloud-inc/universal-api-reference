# Vouchsafe: Native API Reference

A consolidated summary of Vouchsafe's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://app.vouchsafe.id/docs
- **API base URL:** `https://app.vouchsafe.id/api/v1`

## Authentication

### Client ID + Client Secret

Exchange a Vouchsafe client ID and client secret for an access token.

### Credentials

- **Client ID:** `clientId` · required · Your Vouchsafe client ID from the API integrations page.
- **Client Secret:** `clientSecret` · required · Your Vouchsafe client secret from the API integrations page.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://help.vouchsafe.id/en/articles/11979712-how-do-i-authenticate-with-the-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Alert Account Detail](actions/get-alert-account-detail.md) | `GET /alerts/accounts/:id` | [docs](https://app.vouchsafe.id/docs) |
| [Get Artefact](actions/get-artefact.md) | `GET /artefacts/:artefact_key` | [docs](https://app.vouchsafe.id/docs) |
| [Get Flow](actions/get-flow.md) | `GET /flows/:id` | [docs](https://app.vouchsafe.id/docs) |
| [Get Team](actions/get-team.md) | `GET /team` | [docs](https://app.vouchsafe.id/docs) |
| [Get Verification](actions/get-verification.md) | `GET /verifications/:id` | [docs](https://help.vouchsafe.id/en/articles/11979589-quick-start-guide) |
| [List Alert Accounts](actions/list-alert-accounts.md) | `GET /alerts/accounts` | [docs](https://app.vouchsafe.id/docs) |
| [List Flows](actions/list-flows.md) | `GET /flows` | [docs](https://app.vouchsafe.id/docs) |
| [List Verifications](actions/list-verifications.md) | `GET /verifications` | [docs](https://app.vouchsafe.id/docs) |
| [Perform Adverse Media Check](actions/perform-adverse-media-check.md) | `POST /adverse-media` | [docs](https://app.vouchsafe.id/docs) |
| [Perform AML Smart Lookup](actions/perform-aml-smart-lookup.md) | `POST /smart-lookups` | [docs](https://app.vouchsafe.id/docs) |
| [Perform Credit Bureau Smart Lookup](actions/perform-credit-bureau-smart-lookup.md) | `POST /smart-lookups` | [docs](https://app.vouchsafe.id/docs) |
| [Perform Online Footprint Smart Lookup](actions/perform-online-footprint-smart-lookup.md) | `POST /smart-lookups` | [docs](https://app.vouchsafe.id/docs) |
| [Perform Smart Lookup](actions/perform-smart-lookup.md) | `POST /smart-lookups` | [docs](https://app.vouchsafe.id/docs) |
| [Request Verification](actions/request-verification.md) | `POST /verifications` | [docs](https://help.vouchsafe.id/en/articles/11979589-quick-start-guide) |
| [Toggle Alerts](actions/toggle-alerts.md) | `PATCH /alerts/accounts/:id` | [docs](https://app.vouchsafe.id/docs) |
| [Verify eVisa](actions/verify-evisa.md) | `POST /verify/evisa` | [docs](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api) |
| [Verify Immigration Status](actions/verify-immigration-status.md) | `POST /verify/evisa` | [docs](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api) |
| [Verify Right To Rent](actions/verify-right-to-rent.md) | `POST /verify/evisa` | [docs](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api) |
| [Verify Right To Work](actions/verify-right-to-work.md) | `POST /verify/evisa` | [docs](https://help.vouchsafe.id/en/articles/11882037-how-do-i-use-the-evisa-verification-api) |
