# Update Email with Instantly

Updates an existing email in Instantly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/emails/:id`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Update Email](https://developer.instantly.ai/api/v2/email/patchemail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Email UUID. |
| `is_unread` | body | `number` | no | Unread flag. |
| `reminder_ts` | body | `date` | no | Reminder timestamp. |
