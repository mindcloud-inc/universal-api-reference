# List Email Logs with Zoho ZeptoMail

Retrieves email logs from Zoho ZeptoMail.

## Endpoint

- **Method:** `GET`
- **Path:** `email`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [List Email Logs](https://www.zoho.com/zeptomail/help/api/get-email-logs.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bcc` | query | `string` | no | BCC recipient address to filter by. |
| `cc` | query | `string` | no | CC recipient address to filter by. |
| `client_reference` | query | `string` | no | Client reference identifier to filter by. |
| `date_from` | query | `string` | no | Start of the log search window. |
| `date_to` | query | `string` | no | End of the log search window. |
| `from` | query | `string` | no | Sender address to filter by. |
| `is_delivered` | query | `boolean` | no | Filter for delivered email logs. |
| `is_hb` | query | `boolean` | no | Filter for hard bounced email logs. |
| `is_mailfailure` | query | `boolean` | no | Filter for processed failed email logs. |
| `is_sb` | query | `boolean` | no | Filter for soft bounced email logs. |
| `limit` | query | `number` | no | Maximum number of log records to return. |
| `mailagent_key` | query | `string` | no | Agent alias to filter email logs. |
| `offset` | query | `number` | no | Number of log records to skip. |
| `recipient` | query | `string` | no | Recipient address across delivery fields. |
| `request_id` | query | `string` | no | Request identifier of the email. |
| `subject` | query | `string` | no | Email subject to filter by. |
| `to` | query | `string` | no | Recipient address to filter by. |
