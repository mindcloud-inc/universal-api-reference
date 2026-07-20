# List Contacts with Remindlo

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.remindlo.co.uk/v1`
- **Official documentation:** [List Contacts](https://www.remindlo.co.uk/help/sms-reminder-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `created_after` | query | `date` | no |
| `has_phone` | query | `boolean` | no |
| `is_recurrent` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `marketing_consent` | query | `boolean` | no |
| `next_due_after` | query | `date` | no |
| `next_due_before` | query | `date` | no |
| `offset` | query | `number` | no |
| `search` | query | `string` | no |
| `sort_by` | query | `string` | no |
| `sort_order` | query | `string` | no |
