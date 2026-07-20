# Update Email with Resend

Updates an existing email in Resend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/emails/:id`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Update Email](https://resend.com/docs/api-reference/emails/update-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Email identifier. |
| `scheduled_at` | body | `string` | no | Updated scheduled send time. |
