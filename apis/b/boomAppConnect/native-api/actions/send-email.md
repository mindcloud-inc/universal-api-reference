# Send Email with boomApp Connect

Creates an email message in boomApp Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/flat/email`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Send Email](https://learn.microsoft.com/en-us/connectors/boomappconnect/#email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Sender ID displayed in the recipient inbox. |
| `email_subject` | body | `string` | yes | Email subject displayed in the recipient inbox. Required for successful runtime submission. |
| `message_content` | body | `string` | yes | Email body content. Required for successful runtime submission. |
| `email_address[]` | body | `array<string>` | yes | Recipient email addresses. Required for successful runtime submission. |
| `validity_period` | body | `number` | no | Validity period in days. |
| `open_ticket` | body | `boolean` | no | Set true to enable an open ticket for multiple responses. |
| `email_responses` | body | `string` | no | Email address to forward message responses. |
| `push_responses` | body | `string` | no | Callback URL for posted responses. |
| `unique_identifier` | body | `string` | no | Customer-side dedupe identifier. |
| `campaign_name` | body | `string` | no | Optional campaign grouping name. |
| `custom_parameter` | body | `string` | no | Optional custom reference value. |
