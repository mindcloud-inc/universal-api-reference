# Create Reporting Batch with Lasso X

Creates a reporting batch in Lasso X.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/reporting/batches`
- **Base URL:** `https://api.lassox.com`
- **Official documentation:** [Create Reporting Batch](https://docs.lassox.com/module-apis/reporting/#schedule-a-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchName` | body | `string` | yes | Name of the reporting batch. |
| `type` | body | `string` | yes | Report type, for example Revision. |
| `format` | body | `string` | yes | Required report filename format. Supports Lasso variables such as {cvr}, {name}, {type}, {rundate}, and {balanceday}. |
| `items[]` | body | `array<object>` | yes | Reports to generate in the batch. Each item must include cvr and may include format and internalCustomerId. |
| `notificationEmail` | body | `string` | no | Optional email for report completion notifications. |
| `notificationWebhookUrl` | body | `string` | no | Optional webhook URL for report completion notifications. |
| `scheduledTime` | body | `date` | no | Optional scheduled time for the batch. |
