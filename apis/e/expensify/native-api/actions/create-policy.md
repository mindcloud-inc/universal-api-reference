# Create Policy with Expensify

Creates a new policy in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Create Policy](https://integrations.expensify.com/Integration-Server/doc/#policy-creator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyName` | body | `string` | yes | The name of the policy to create. |
| `plan` | body | `string` | no | Optional policy plan. Accepted values: `0`, `1`. |
