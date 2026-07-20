# Make Voice Call with boomApp Connect

Creates a text-to-speech voice call in boomApp Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/flat/voice`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Make Voice Call](https://learn.microsoft.com/en-us/connectors/boomappconnect/#voice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_intro` | body | `string` | yes | Welcome message played when the call is answered. Required for successful runtime submission. |
| `message_content` | body | `string` | yes | Main voice message body. Required for successful runtime submission. |
| `recipient_address[]` | body | `array<object>` | yes | Recipient phone numbers as objects with a number field. Required for successful runtime submission. |
| `voice_thank_you` | body | `string` | no | Exit message played after the recipient listens or responds. |
| `voice_retries` | body | `number` | no | Retry attempts, maximum 3 per connector schema. |
| `voice_delay` | body | `number` | no | Interval between retry attempts in minutes. |
| `email_responses` | body | `string` | no | Email address to forward response details. |
| `push_responses` | body | `string` | no | Webhook to push response details. |
| `unique_identifier` | body | `string` | no | Customer-side dedupe identifier. |
| `locale` | body | `string` | no | Voice locale, accent, or language. |
