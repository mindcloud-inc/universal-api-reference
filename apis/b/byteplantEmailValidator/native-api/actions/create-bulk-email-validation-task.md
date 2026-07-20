# Create Bulk Email Validation Task with Byteplant Email Validator

Creates a bulk email validation task in Byteplant Email Validator.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/bulk-verify`
- **Base URL:** `https://api.email-validator.net`
- **Official documentation:** [Create Bulk Email Validation Task](https://www.byteplant.com/email-validator/api.html#bulk-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailsCsv` | body | `string` | yes | CSV content with an `Email` header and one email address per row. |
| `TaskName` | query | `string` | no | Optional name for the bulk validation task. |
| `ValidationMode` | query | `list` | no | Optional validation mode. Express retries unavailable servers for 2 hours; extensive retries for 72 hours. Accepted values: `express`, `extensive`. |
| `NotifyEmail` | query | `string` | no | Optional email address to receive completion notifications for this task. |
| `NotifyURL` | query | `string` | no | Optional URL to receive a completion notification with the task id. |
