# IdentityCheck: Native API Reference

A consolidated summary of IdentityCheck's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740
- **API base URL:** `https://identity.stackgo.io/api`

## Authentication

### API Key (Basic Auth)

Use your IdentityCheck API key as Username. Leave Password blank. When generating the key in IdentityCheck, select all scopes.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740?pvs=4)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Verification](actions/cancel-verification.md) | `DELETE /verification/cancel/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Create Direct Verification](actions/create-direct-verification.md) | `POST /direct-verification` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Create Form](actions/create-form.md) | `POST /form` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Create Pre-Verification Setting](actions/create-pre-verification-setting.md) | `POST /pre-verification-settings` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Generate KYB Report](actions/generate-kyb-report.md) | `POST /v1/verification/namescan/kyb` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Admin Response](actions/get-admin-response.md) | `GET /response/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Form](actions/get-form.md) | `GET /form/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Pre-Verification Setting](actions/get-pre-verification-setting.md) | `GET /pre-verification-settings/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Public Onboarding Form](actions/get-public-onboarding-form.md) | `GET /public/onboarding/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Public Response](actions/get-public-response.md) | `GET /public/response/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Public Verification](actions/get-public-verification.md) | `GET /public/verification/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Verification](actions/get-verification.md) | `GET /verification/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Verification Chart](actions/get-verification-chart.md) | `GET /verification/chart` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Get Webhook Integration Settings](actions/get-webhook-integration-settings.md) | `GET /integration/webhook` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [List Forms](actions/list-forms.md) | `GET /form` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [List Pre-Verification Settings](actions/list-pre-verification-settings.md) | `GET /pre-verification-settings` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [List Verifications](actions/list-verifications.md) | `GET /verification` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Request Webhook Portal](actions/request-webhook-portal.md) | `POST /webhook` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Submit Public Onboarding Form](actions/submit-public-onboarding-form.md) | `POST /public/onboarding/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Submit Public Response](actions/submit-public-response.md) | `POST /public/response/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Submit Tranche 2 Consent](actions/submit-tranche2-consent.md) | `POST /public/verification/{id}/tranche2/consent` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Update Form](actions/update-form.md) | `PATCH /form/{id}` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Update Webhook Integration Settings](actions/update-webhook-integration-settings.md) | `POST /integration/webhook` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
| [Validate Proof Of Address](actions/validate-proof-of-address.md) | `POST /public/poa-check` | [docs](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740) |
