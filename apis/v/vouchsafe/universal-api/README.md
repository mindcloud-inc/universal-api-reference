# <img src="https://images.mindcloud.co/apps/icons/cropped-icon-light-bg-32x32_1775595006324.png" alt="Vouchsafe logo" width="28" height="28"> Vouchsafe: Universal API

Verify identity, onboard customers, prevent fraud, and support compliance

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vouchsafe/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vouchsafe.id/
- **Vendor API docs:** https://app.vouchsafe.id/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Alert Account Detail](actions/get-alert-account-detail.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/get-alert-account-detail?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Account Detail](actions/get-alert-account-detail.md) | GET | Retrieves alert account details from Vouchsafe. |
| [Get Artefact](actions/get-artefact.md) | GET | Retrieves an artefact download link from Vouchsafe. |
| [Get Flow](actions/get-flow.md) | GET | Retrieves a verification flow from Vouchsafe. |
| [Get Verification](actions/get-verification.md) | GET | Retrieves a verification from Vouchsafe. |
| [List Alert Accounts](actions/list-alert-accounts.md) | GET | Retrieves monitored alert accounts from Vouchsafe. |
| [List Flows](actions/list-flows.md) | GET | Retrieves published verification flows from Vouchsafe. |
| [List Verifications](actions/list-verifications.md) | GET | Retrieves a list of verifications from Vouchsafe. |
| [Perform Adverse Media Check](actions/perform-adverse-media-check.md) | POST | Runs an adverse media check in Vouchsafe. |
| [Perform AML Smart Lookup](actions/perform-aml-smart-lookup.md) | POST | Runs an AML smart lookup in Vouchsafe. |
| [Perform Credit Bureau Smart Lookup](actions/perform-credit-bureau-smart-lookup.md) | POST | Runs a credit bureau smart lookup in Vouchsafe. |
| [Perform Online Footprint Smart Lookup](actions/perform-online-footprint-smart-lookup.md) | POST | Runs an online footprint smart lookup in Vouchsafe. |
| [Perform Smart Lookup](actions/perform-smart-lookup.md) | POST | Runs smart lookup checks in Vouchsafe. |
| [Request Verification](actions/request-verification.md) | POST | Creates a verification request in Vouchsafe. |
| [Toggle Alerts](actions/toggle-alerts.md) | PUT | Updates ongoing monitoring for an alert account in Vouchsafe. |
| [Verify eVisa](actions/verify-evisa.md) | POST | Verifies a UK eVisa in Vouchsafe. |
| [Verify Immigration Status](actions/verify-immigration-status.md) | POST | Verifies immigration status with a UK eVisa in Vouchsafe. |
| [Verify Right To Rent](actions/verify-right-to-rent.md) | POST | Verifies right to rent with a UK eVisa in Vouchsafe. |
| [Verify Right To Work](actions/verify-right-to-work.md) | POST | Verifies right to work with a UK eVisa in Vouchsafe. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves the authenticated team from Vouchsafe. |

