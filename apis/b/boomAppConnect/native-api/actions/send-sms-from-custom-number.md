# Send SMS From Custom Number with boomApp Connect

Creates an SMS message from a custom number in boomApp Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/flat/sms3`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Send SMS From Custom Number](https://learn.microsoft.com/en-us/connectors/boomappconnect/#sms-custom-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Numeric sending ID associated to the message. Required for successful runtime submission. |
| `message_content` | body | `string` | yes | Outbound SMS message content. Required for successful runtime submission. |
| `recipient_address[]` | body | `array<object>` | yes | Recipient mobile numbers as objects with a number field. Required for successful runtime submission. |
| `priority` | body | `boolean` | no | Set true to override Social Hours when the account supports it. |
| `unique_identifier` | body | `string` | no | Customer-side dedupe identifier. |
| `campaign_name` | body | `string` | no | Optional campaign grouping name. |
| `custom_parameter` | body | `string` | no | Optional custom reference value. |
