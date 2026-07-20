# Particle: Native API Reference

A consolidated summary of Particle's API configuration and 58 documented operations, with links to official documentation.

- **Official docs:** https://docs.particle.io/reference/cloud-apis/api/
- **API base URL:** `https://api.particle.io`

## Authentication

### Access Token

Use a Particle access token. MindCloud sends it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.particle.io/reference/cloud-apis/api/)

## Endpoints (58 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Call Device Function](actions/call-device-function.md) | `POST /v1/devices/:deviceId/:functionName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#call-a-function) |
| [Create Ledger](actions/create-ledger.md) | `POST /v1/ledgers` | [docs](https://docs.particle.io/reference/cloud-apis/api/#create-a-new-ledger-definition) |
| [Create Logic Function](actions/create-logic-function.md) | `POST /v1/logic/functions` | [docs](https://docs.particle.io/reference/cloud-apis/api/#create-a-new-logic-function) |
| [Create Secret](actions/create-secret.md) | `POST /v1/secrets` | [docs](https://docs.particle.io/reference/cloud-apis/api/#create-a-cloud-secret) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/integrations` | [docs](https://docs.particle.io/reference/cloud-apis/api/#create-a-webhook) |
| [Delete Current Access Token](actions/delete-current-access-token.md) | `DELETE /v1/access_tokens/current` | [docs](https://docs.particle.io/reference/cloud-apis/api/#delete-current-access-token) |
| [Delete Environment Variable](actions/delete-environment-variable.md) | `DELETE /v1/env/:key` | [docs](https://docs.particle.io/reference/cloud-apis/api/#delete-environment-variable) |
| [Delete Integration](actions/delete-integration.md) | `DELETE /v1/integrations/:integrationId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#delete-an-integration) |
| [Delete Ledger](actions/delete-ledger.md) | `DELETE /v1/ledgers/:ledgerName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#archive-a-ledger-definition) |
| [Delete Ledger Instance](actions/delete-ledger-instance.md) | `DELETE /v1/ledgers/:ledgerName/instances/:scopeValue` | [docs](https://docs.particle.io/reference/cloud-apis/api/#delete-ledger-instance) |
| [Delete Logic Function](actions/delete-logic-function.md) | `DELETE /v1/logic/functions/:logicFunctionId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#delete-logic-function) |
| [Delete Secret](actions/delete-secret.md) | `DELETE /v1/secrets/:secretName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#delete-a-cloud-secret) |
| [Delete Webhooks](actions/delete-webhooks.md) | `DELETE /v1/webhooks` | [docs](https://docs.particle.io/reference/cloud-apis/api/) |
| [Get Cellular Network Status](actions/get-cellular-network-status.md) | `GET /v1/sims/:iccid/status` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-cellular-network-status) |
| [Get Current Access Token](actions/get-current-access-token.md) | `GET /v1/access_tokens/current` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-the-current-access-token-information) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/user` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-user) |
| [Get Device](actions/get-device.md) | `GET /v1/devices/:deviceId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-device-information) |
| [Get Device Variable](actions/get-device-variable.md) | `GET /v1/devices/:deviceId/:varName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-a-variable-value) |
| [Get Integration](actions/get-integration.md) | `GET /v1/integrations/:integrationId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-integration) |
| [Get Ledger](actions/get-ledger.md) | `GET /v1/ledgers/:ledgerName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-ledger-definition) |
| [Get Ledger Instance](actions/get-ledger-instance.md) | `GET /v1/ledgers/:ledgerName/instances/:scopeValue` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-ledger-instance) |
| [Get Ledger Version](actions/get-ledger-version.md) | `GET /v1/ledgers/:ledgerName/instances/:scopeValue/versions/:version` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-ledger-instance-version) |
| [Get Library](actions/get-library.md) | `GET /v1/libraries/:libraryName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-library-details) |
| [Get Logic Function](actions/get-logic-function.md) | `GET /v1/logic/functions/:logicFunctionId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-logic-function) |
| [Get Secret](actions/get-secret.md) | `GET /v1/secrets/:secretName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-cloud-secret-by-name) |
| [Get SIM Data Usage](actions/get-sim-data-usage.md) | `GET /v1/sims/:iccid/data_usage` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-data-usage) |
| [Get SIM Information](actions/get-sim-information.md) | `GET /v1/sims/:iccid` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-sim-information) |
| [Import Devices into Product](actions/import-devices-into-product.md) | `POST /v1/products/:productIdOrSlug/devices` | [docs](https://docs.particle.io/reference/cloud-apis/api/#import-devices-into-product) |
| [List Account Events](actions/list-account-events.md) | `GET /v1/events/:eventPrefix` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-a-stream-of-events) |
| [List Device Events](actions/list-device-events.md) | `GET /v1/devices/:deviceId/events/:eventPrefix` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-a-stream-of-events-for-a-device) |
| [List Devices](actions/list-devices.md) | `GET /v1/devices` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-devices) |
| [List Environment Variables](actions/list-environment-variables.md) | `GET /v1/env` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-environment-variables) |
| [List Integrations](actions/list-integrations.md) | `GET /v1/integrations` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-integrations) |
| [List Ledger Instances](actions/list-ledger-instances.md) | `GET /v1/ledgers/:ledgerName/instances` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-ledger-instances) |
| [List Ledger Versions](actions/list-ledger-versions.md) | `GET /v1/ledgers/:ledgerName/instances/:scopeValue/versions` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-ledger-instance-versions) |
| [List Ledgers](actions/list-ledgers.md) | `GET /v1/ledgers` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-ledger-definitions) |
| [List Libraries](actions/list-libraries.md) | `GET /v1/libraries` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-libraries) |
| [List Library Versions](actions/list-library-versions.md) | `GET /v1/libraries/:libraryName/versions` | [docs](https://docs.particle.io/reference/cloud-apis/api/#get-library-versions) |
| [List Logic Functions](actions/list-logic-functions.md) | `GET /v1/logic/functions` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-logic-functions) |
| [List Products](actions/list-products.md) | `GET /v1/user/products` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-products) |
| [List Secrets](actions/list-secrets.md) | `GET /v1/secrets` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-cloud-secrets) |
| [List SIM Cards](actions/list-sim-cards.md) | `GET /v1/sims` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-sim-cards) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/webhooks` | [docs](https://docs.particle.io/reference/cloud-apis/api/#list-integrations) |
| [Look Up Device Identification by Serial Number](actions/look-up-device-identification-by-serial-number.md) | `GET /v1/serial_numbers/:serialNumber` | [docs](https://docs.particle.io/reference/cloud-apis/api/#look-up-device-identification-from-a-serial-number) |
| [Ping Device](actions/ping-device.md) | `PUT /v1/devices/:deviceId/ping` | [docs](https://docs.particle.io/reference/cloud-apis/api/#ping-a-device) |
| [Release SIM from Account](actions/release-sim-from-account.md) | `DELETE /v1/sims/:iccid` | [docs](https://docs.particle.io/reference/cloud-apis/api/#release-sim-from-account) |
| [Rename Device](actions/rename-device.md) | `PUT /v1/devices/:deviceId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#rename-a-device) |
| [Render Environment Variables](actions/render-environment-variables.md) | `GET /v1/env/render` | [docs](https://docs.particle.io/reference/cloud-apis/api/#render-environment-variables) |
| [Roll Out Environment Variables](actions/roll-out-environment-variables.md) | `POST /v1/env/rollout` | [docs](https://docs.particle.io/reference/cloud-apis/api/#start-environment-variables-rollout) |
| [Test Integration](actions/test-integration.md) | `POST /v1/integrations/:integrationId/test` | [docs](https://docs.particle.io/reference/cloud-apis/api/#test-an-integration) |
| [Unclaim Device](actions/unclaim-device.md) | `DELETE /v1/devices/:deviceId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#unclaim-device) |
| [Update Integration](actions/update-integration.md) | `PUT /v1/integrations/:integrationId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#edit-a-webhook) |
| [Update Ledger](actions/update-ledger.md) | `PUT /v1/ledgers/:ledgerName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#update-ledger-definition) |
| [Update Ledger Instance](actions/update-ledger-instance.md) | `PUT /v1/ledgers/:ledgerName/instances/:scopeValue` | [docs](https://docs.particle.io/reference/cloud-apis/api/#set-the-ledger-instance-data) |
| [Update Logic Function](actions/update-logic-function.md) | `PUT /v1/logic/functions/:logicFunctionId` | [docs](https://docs.particle.io/reference/cloud-apis/api/#update-logic-function) |
| [Update Secret](actions/update-secret.md) | `PUT /v1/secrets/:secretName` | [docs](https://docs.particle.io/reference/cloud-apis/api/#create-or-update-the-value-of-a-cloud-secret) |
| [Update SIM](actions/update-sim.md) | `PUT /v1/sims/:iccid` | [docs](https://docs.particle.io/reference/cloud-apis/api/) |
| [Upsert Environment Variable](actions/upsert-environment-variable.md) | `PUT /v1/env/:key` | [docs](https://docs.particle.io/reference/cloud-apis/api/#set-environment-variable) |
