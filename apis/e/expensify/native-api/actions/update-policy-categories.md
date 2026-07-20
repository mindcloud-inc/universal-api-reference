# Update Policy Categories with Expensify

Updates policy categories in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Update Policy Categories](https://integrations.expensify.com/Integration-Server/doc/#policy-updater)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | body | `string` | yes | The Expensify policy ID to update. |
| `mode` | body | `string` | yes | Whether to merge or replace categories. Accepted values: `0`, `1`. |
| `categoriesJson` | body | `string` | yes | JSON array of category objects to apply, for example [{"name":"Travel","enabled":true}]. |
