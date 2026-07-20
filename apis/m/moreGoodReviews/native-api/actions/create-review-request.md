# Create Review Request with More Good Reviews

Creates a review request in More Good Reviews.

## Endpoint

- **Method:** `POST`
- **Path:** `/beacon/asks`
- **Base URL:** `https://api.moregoodreviews.com`
- **Official documentation:** [Create Review Request](https://docs.moregoodreviews.com/platform/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The customer's email address. |
| `phone` | body | `string` | no | The customer's phone number. |
| `channels[]` | body | `array<string>` | no | Include email, sms, or both channels. |
| `reminders_count` | body | `number` | no | 0 - 3 reminders. |
| `asked_at` | body | `date` | no | The date to schedule the request. If null, it will send immediately. |
