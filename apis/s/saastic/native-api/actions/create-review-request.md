# Create Review Request with Saastic

Creates a review request in Saastic.

## Endpoint

- **Method:** `POST`
- **Path:** `/beacon/asks`
- **Base URL:** `https://api.moregoodreviews.com`
- **Official documentation:** [Create Review Request](https://docs.moregoodreviews.com/platform/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The customer's email address. Required when phone is not provided. |
| `phone` | body | `string` | no | The customer's phone number. Required when email is not provided. |
| `channels[]` | body | `array<string>` | no | Include email, sms, or both channels. |
| `reminders_count` | body | `number` | no | Number of reminders to send, from 0 to 3. |
| `asked_at` | body | `date` | no | The date to schedule the request. If null, it sends immediately. |
