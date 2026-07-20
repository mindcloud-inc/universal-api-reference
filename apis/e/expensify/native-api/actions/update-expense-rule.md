# Update Expense Rule with Expensify

Updates an existing expense rule in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Update Expense Rule](https://integrations.expensify.com/Integration-Server/doc/#expense-rules-updater)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | body | `string` | yes | The policy to update the rule on. |
| `employeeEmail` | body | `string` | yes | The policy member who should receive the expense rule. |
| `ruleId` | body | `string` | yes | The expense rule ID to update. |
| `actionsJson` | body | `string` | yes | JSON object containing supported rule actions, for example {"tag":"Tag Name"}. |
