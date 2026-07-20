# Run Reconciliation Export with Expensify

Retrieves a reconciliation export from Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Run Reconciliation Export](https://integrations.expensify.com/Integration-Server/doc/#reconciliation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | The domain to run reconciliation for. |
| `startDate` | body | `string` | yes | The inclusive reconciliation start date in yyyy-mm-dd format. |
| `endDate` | body | `string` | yes | The inclusive reconciliation end date in yyyy-mm-dd format. |
| `reconciliationType` | body | `string` | yes | Unreported or All. Accepted values: `0`, `1`. |
| `fileExtension` | body | `string` | yes | The reconciliation export format. Accepted values: `0`, `1`, `2`, `3`. |
