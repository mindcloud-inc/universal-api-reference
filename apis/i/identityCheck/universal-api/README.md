# <img src="https://images.mindcloud.co/apps/icons/identity-check_1774549381061.png" alt="IdentityCheck logo" width="28" height="28"> IdentityCheck: Universal API

Create verifications, run KYB checks, and manage onboarding forms

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/identityCheck/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://identity.stackgo.io
- **Vendor API docs:** https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Verifications](actions/list-verifications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/list-verifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Verification](actions/cancel-verification.md) | DELETE |  |
| [Create Direct Verification](actions/create-direct-verification.md) | POST |  |
| [Create Pre-Verification Setting](actions/create-pre-verification-setting.md) | POST |  |
| [Get Pre-Verification Setting](actions/get-pre-verification-setting.md) | GET |  |
| [Get Public Verification](actions/get-public-verification.md) | GET |  |
| [Get Verification](actions/get-verification.md) | GET |  |
| [List Pre-Verification Settings](actions/list-pre-verification-settings.md) | GET |  |
| [List Verifications](actions/list-verifications.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Validate Proof Of Address](actions/validate-proof-of-address.md) | POST |  |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Admin Response](actions/get-admin-response.md) | GET |  |
| [Submit Public Onboarding Form](actions/submit-public-onboarding-form.md) | POST |  |
| [Submit Public Response](actions/submit-public-response.md) | POST |  |
| [Submit Tranche 2 Consent](actions/submit-tranche2-consent.md) | POST |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST |  |
| [Get Form](actions/get-form.md) | GET |  |
| [Get Public Onboarding Form](actions/get-public-onboarding-form.md) | GET |  |
| [Get Public Response](actions/get-public-response.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET |  |
| [Update Form](actions/update-form.md) | PUT |  |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook Integration Settings](actions/get-webhook-integration-settings.md) | GET |  |
| [Request Webhook Portal](actions/request-webhook-portal.md) | POST |  |
| [Update Webhook Integration Settings](actions/update-webhook-integration-settings.md) | PUT |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Generate KYB Report](actions/generate-kyb-report.md) | POST |  |
| [Get Verification Chart](actions/get-verification-chart.md) | GET |  |

