# Update Mailbox with Atriomail

## Endpoint

- **Method:** `PUT`
- **Path:** `/mailboxes/:mailboxId`
- **Base URL:** `https://system.atriomail.com/api/v1`
- **Official documentation:** [Update Mailbox](https://system.atriomail.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailboxId` | path | `number` | yes | The AtrioMail mailbox ID. |
| `name` | body | `string` | no | The updated mailbox display name. |
