# Create Webhook with Avaza

Creates a new webhook in Avaza.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Webhook`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [Create Webhook](https://api.avaza.com/#!/Webhook/Webhook_Post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | The URL that should be notified of the event. |
| `event` | body | `string` | yes | The event code to be notified about. Possible values: company_created, company_deleted, company_updated, contact_created, contact_deleted, contact_updated, invoice_created, invoice_sent, invoice_updated, invoice_deleted, project_created, project_deleted, project_updated, task_created, task_updated, task_deleted, timesheet_created, timesheet_deleted, timesheet_updated, bill_created, bill_updated, estimate_created, estimate_updated, estimate_deleted |
| `secret` | body | `string` | no | Optional Secret string (255 char max). If provided, the secret will be BASE 64 encoded and used as a basic authentication http header with webhook notifications. i.e. Authorization Basic [BASE64 of Secret]" |
