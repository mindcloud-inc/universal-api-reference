# Create Lead with SWELLEnterprise

Creates a new lead in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/leads`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Lead](https://dashboard.swellsystem.com/docs#crm-leads-POSTapi-v1-crm-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The lead title. |
| `value` | body | `number` | no | The lead value. |
| `status_id` | body | `number` | yes | The status ID. |
| `source_id` | body | `number` | no | The referral source ID. |
| `company_id` | body | `number` | no | The company ID. |
| `assigned_to` | body | `number` | no | The assigned user ID. |
| `description` | body | `string` | no | The lead description. |
