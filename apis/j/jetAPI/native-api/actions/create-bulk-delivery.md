# Create Bulk Delivery with JetAPI

Creates a new bulk delivery in JetAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/bulk_delivery`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Create Bulk Delivery](https://docs.jetapi.io/#1f668b73-8439-43d2-bb7f-95942c5da96d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | yes | Message text. |
| `phones_numbers[]` | query | `array<string>` | yes | Recipient phone numbers in international format. |
| `sender_name` | query | `string` | no | — |
| `scheduled_at` | query | `date` | no | UTC datetime in YYYY-MM-DD HH:MM:SS. |
| `utm_mark` | query | `string` | no | — |
| `dispatch_routing[]` | query | `array<string>` | no | — |
| `usernames[]` | query | `array<string>` | no | — |
| `tdlib_user_id` | query | `string` | no | — |
