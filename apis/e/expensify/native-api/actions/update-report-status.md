# Update Report Status with Expensify

Updates a report status in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Update Report Status](https://integrations.expensify.com/Integration-Server/doc/#report-status-updater)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `string` | yes | The target report status. Expensify currently supports REIMBURSED. |
| `paymentSource` | body | `string` | no | Optional payment source label. |
| `reportIdList` | body | `string` | yes | Comma-separated report IDs to update. |
