# <img src="https://images.mindcloud.co/apps/icons/particle-icon-512_1775584831132.png" alt="Particle logo" width="28" height="28"> Particle: Universal API

Manage Particle Cloud resources including users, devices, diagnostics, integrations, ledgers, logic functions, products, SIMs, and environment variables.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/particle/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 58
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://particle.io
- **Vendor API docs:** https://docs.particle.io/reference/cloud-apis/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/particle/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (58)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Delete Current Access Token](actions/delete-current-access-token.md) | DELETE |  |
| [Get Current Access Token](actions/get-current-access-token.md) | GET |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Call Device Function](actions/call-device-function.md) | PUT |  |
| [Get Device](actions/get-device.md) | GET |  |
| [Get Device Variable](actions/get-device-variable.md) | GET |  |
| [Import Devices into Product](actions/import-devices-into-product.md) | POST |  |
| [List Device Events](actions/list-device-events.md) | GET |  |
| [List Devices](actions/list-devices.md) | GET |  |
| [Ping Device](actions/ping-device.md) | PUT |  |
| [Rename Device](actions/rename-device.md) | PUT |  |
| [Unclaim Device](actions/unclaim-device.md) | DELETE |  |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Create Secret](actions/create-secret.md) | POST |  |
| [Delete Secret](actions/delete-secret.md) | DELETE |  |
| [Get Secret](actions/get-secret.md) | GET |  |
| [List Secrets](actions/list-secrets.md) | GET |  |
| [Update Secret](actions/update-secret.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Ledger](actions/create-ledger.md) | POST |  |
| [Create Logic Function](actions/create-logic-function.md) | POST |  |
| [Delete Environment Variable](actions/delete-environment-variable.md) | DELETE |  |
| [Delete Integration](actions/delete-integration.md) | DELETE |  |
| [Delete Ledger](actions/delete-ledger.md) | DELETE |  |
| [Delete Ledger Instance](actions/delete-ledger-instance.md) | DELETE |  |
| [Delete Logic Function](actions/delete-logic-function.md) | DELETE |  |
| [Get Cellular Network Status](actions/get-cellular-network-status.md) | GET |  |
| [Get Integration](actions/get-integration.md) | GET |  |
| [Get Ledger](actions/get-ledger.md) | GET |  |
| [Get Ledger Instance](actions/get-ledger-instance.md) | GET |  |
| [Get Ledger Version](actions/get-ledger-version.md) | GET |  |
| [Get Library](actions/get-library.md) | GET |  |
| [Get Logic Function](actions/get-logic-function.md) | GET |  |
| [Get SIM Data Usage](actions/get-sim-data-usage.md) | GET |  |
| [Get SIM Information](actions/get-sim-information.md) | GET |  |
| [List Account Events](actions/list-account-events.md) | GET |  |
| [List Environment Variables](actions/list-environment-variables.md) | GET |  |
| [List Integrations](actions/list-integrations.md) | GET |  |
| [List Ledger Instances](actions/list-ledger-instances.md) | GET |  |
| [List Ledger Versions](actions/list-ledger-versions.md) | GET |  |
| [List Ledgers](actions/list-ledgers.md) | GET |  |
| [List Libraries](actions/list-libraries.md) | GET |  |
| [List Library Versions](actions/list-library-versions.md) | GET |  |
| [List Logic Functions](actions/list-logic-functions.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |
| [List SIM Cards](actions/list-sim-cards.md) | GET |  |
| [Look Up Device Identification by Serial Number](actions/look-up-device-identification-by-serial-number.md) | GET |  |
| [Release SIM from Account](actions/release-sim-from-account.md) | DELETE |  |
| [Render Environment Variables](actions/render-environment-variables.md) | GET |  |
| [Roll Out Environment Variables](actions/roll-out-environment-variables.md) | PUT |  |
| [Test Integration](actions/test-integration.md) | PUT |  |
| [Update Integration](actions/update-integration.md) | PUT |  |
| [Update Ledger](actions/update-ledger.md) | PUT |  |
| [Update Ledger Instance](actions/update-ledger-instance.md) | PUT |  |
| [Update Logic Function](actions/update-logic-function.md) | PUT |  |
| [Update SIM](actions/update-sim.md) | PUT |  |
| [Upsert Environment Variable](actions/upsert-environment-variable.md) | PUT |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhooks](actions/delete-webhooks.md) | DELETE |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

