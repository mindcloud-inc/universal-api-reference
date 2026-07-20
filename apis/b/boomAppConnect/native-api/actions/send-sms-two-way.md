# Send SMS Two-Way with boomApp Connect

Creates a two-way SMS message in boomApp Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/flat/sms2`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Send SMS Two-Way](https://learn.microsoft.com/en-us/connectors/boomappconnect/#sms-two-way)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | body | `string` | yes | Conversation ID used to group related two-way messages and replies. Required for successful runtime submission. |
| `message_content` | body | `string` | yes | Outbound SMS message content. Required for successful runtime submission. |
| `recipient_address[]` | body | `array<object>` | yes | Recipient mobile numbers as objects with a number field. Required for successful runtime submission. |
| `validity_period` | body | `number` | no | Validity period in days. |
| `open_ticket` | body | `boolean` | no | Set true to allow multiple responses to match the originating message. |
| `email_responses` | body | `string` | no | Email address for forwarded responses. |
| `push_responses` | body | `string` | no | Callback URL for posted responses. |
| `priority` | body | `boolean` | no | Set true to override Social Hours when the account supports it. |
| `unique_identifier` | body | `string` | no | Customer-side dedupe identifier. |
| `campaign_name` | body | `string` | no | Optional campaign grouping name. |
| `custom_parameter` | body | `string` | no | Optional custom reference value. |
