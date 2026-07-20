# Send SMS One-Way with boomApp Connect

Creates a one-way SMS message in boomApp Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/flat/sms1`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Send SMS One-Way](https://learn.microsoft.com/en-us/connectors/boomappconnect/#sms-one-way)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Originating ID for the one-way SMS message. Required for successful runtime submission. |
| `message_content` | body | `string` | yes | Outbound SMS message content. Required for successful runtime submission. |
| `recipient_address[]` | body | `array<object>` | yes | Recipient mobile numbers as objects with a number field. Required for successful runtime submission. |
| `priority` | body | `boolean` | no | Set true to override Social Hours when the account supports it. |
| `unique_identifier` | body | `string` | no | Customer-side dedupe identifier. |
| `campaign_name` | body | `string` | no | Optional campaign grouping name. |
| `custom_parameter` | body | `string` | no | Optional custom reference value. |
