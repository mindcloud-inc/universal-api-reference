# Create Webhook with Remindlo

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.remindlo.co.uk/v1`
- **Official documentation:** [Create Webhook](https://www.remindlo.co.uk/help/sms-reminder-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event_types[]` | body | `array<string>` | yes |
| `name` | body | `string` | yes |
| `target_url` | body | `string` | yes |
