# Send Message with Remindlo

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://api.remindlo.co.uk/v1`
- **Official documentation:** [Send Message](https://www.remindlo.co.uk/help/sms-reminder-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Maximum length: 1600. |
| `channel` | body | `string` | no | — |
| `contact_id` | body | `string` | yes | — |
