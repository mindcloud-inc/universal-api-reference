# Send Email with Mailrelay

Sends an email to one or more recipients through Mailrelay.

## Endpoint

- **Method:** `POST`
- **Path:** `send_emails`
- **Base URL:** `https://{accountDomain}/api/v1`
- **Official documentation:** [Send Email](https://apidocs.mailrelay.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | From email address. |
| `email` | body | `string` | yes | Recipient email address. |
| `from` | body | `object` | yes | From header object. |
| `html_part` | body | `string` | no | HTML email content. |
| `name` | body | `string` | no | From display name. |
| `name` | body | `string` | no | Recipient display name. |
| `subject` | body | `string` | yes | Email subject. |
| `text_part` | body | `string` | no | Plain-text email content. |
| `text_part_auto` | body | `boolean` | no | Automatically generate plain-text content from HTML. |
| `to[]` | body | `array` | yes | Recipient list. |
