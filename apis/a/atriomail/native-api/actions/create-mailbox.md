# Create Mailbox with Atriomail

## Endpoint

- **Method:** `POST`
- **Path:** `/mailboxes`
- **Base URL:** `https://system.atriomail.com/api/v1`
- **Official documentation:** [Create Mailbox](https://system.atriomail.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | body | `number` | yes | The AtrioMail domain ID that owns the mailbox. |
| `local_part` | body | `string` | yes | The mailbox local part before the @ symbol. |
| `name` | body | `string` | yes | The mailbox display name. |
| `password` | body | `string` | yes | The mailbox password. |
