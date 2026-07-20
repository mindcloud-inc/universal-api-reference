# Update Mailbox with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/mailboxes/:mailbox_id`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Update Mailbox](https://help.parsio.io/public-api/parsio-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `string` | yes | Parsio mailbox ID. |
| `name` | body | `string` | no | Mailbox name. |
| `email_prefix` | body | `string` | yes | Mailbox email prefix. |
| `process_attachments` | body | `boolean` | no | Whether to store email attachments. |
| `collect_emails` | body | `boolean` | no | Whether to collect email addresses automatically. |
| `alert_email_h` | body | `number` | no | Email alert frequency in hours. |
