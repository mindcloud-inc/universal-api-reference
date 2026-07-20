# Create Expenses with Expensify

Creates new expenses in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Create Expenses](https://integrations.expensify.com/Integration-Server/doc/#expense-creator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employeeEmail` | body | `string` | yes | The account that should receive the created expenses. |
| `transactionListJson` | body | `string` | yes | JSON array of expense objects to create. |
