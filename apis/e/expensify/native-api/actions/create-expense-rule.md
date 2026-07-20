# Create Expense Rule with Expensify

Creates a new expense rule in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Create Expense Rule](https://integrations.expensify.com/Integration-Server/doc/#expense-rules-creator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | body | `string` | yes | The policy to create the rule on. |
| `employeeEmail` | body | `string` | yes | The policy member who should receive the expense rule. |
| `actionsJson` | body | `string` | yes | JSON object containing supported rule actions, for example {"tag":"Tag Name"}. |
