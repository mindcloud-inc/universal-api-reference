# Estimate Personalized Message with SMS.to

Retrieves a cost estimate for personalized SMS messages.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/estimate`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Estimate Personalized Message](https://developers.sms.to/#2c63629b-5414-48ef-8b9b-cd902c23275d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of message objects with recipient phone numbers. |
| `messages[].message` | body | `string` | yes | Your message for the specified phone number. |
| `messages[].to` | body | `string` | no | The recipient phone number. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
