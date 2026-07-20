# Upsert Contact with Remindlo

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.remindlo.co.uk/v1`
- **Official documentation:** [Upsert Contact](https://www.remindlo.co.uk/help/sms-reminder-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaign_ids[]` | body | `array<string>` | no |
| `custom_fields` | body | `object` | no |
| `email` | body | `string` | no |
| `first_name` | body | `string` | no |
| `is_recurrent` | body | `boolean` | no |
| `last_name` | body | `string` | no |
| `last_service_at` | body | `date` | no |
| `marketing_consent` | body | `boolean` | no |
| `next_due_at` | body | `date` | no |
| `note` | body | `string` | no |
| `phone` | body | `string` | no |
| `recurrent_interval_unit` | body | `string` | no |
| `recurrent_interval_value` | body | `number` | no |
| `tags[]` | body | `array<string>` | no |
