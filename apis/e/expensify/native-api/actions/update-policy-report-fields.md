# Update Policy Report Fields with Expensify

Updates policy report fields in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Update Policy Report Fields](https://integrations.expensify.com/Integration-Server/doc/#policy-updater)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | body | `string` | yes | The Expensify policy ID to update. |
| `mode` | body | `string` | yes | Whether to merge or replace report fields. Accepted values: `0`, `1`. |
| `reportFieldsJson` | body | `string` | yes | JSON array of report field objects, for example [{"name":"Cost Center","type":"dropdown","values":["A","B"]}]. |
