# Create Job with Housecall Pro

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Create Job](https://docs.housecallpro.com/docs/housecall-public-api/2dcf481ed7d69-create-a-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | — |
| `address_id` | body | `string` | yes | — |
| `notes` | body | `string` | no | — |
| `lead_source` | body | `string` | no | — |
| `invoice_number` | body | `number` | no | Invoice number must be unique across all company jobs. If blank, one is generated automatically. |
| `schedule` | body | `object` | no | Scheduling details for the job. |
| `assigned_employee_ids[]` | body | `array<string>` | no | — |
| `line_items[]` | body | `array<object>` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `job_fields` | body | `object` | no | — |
