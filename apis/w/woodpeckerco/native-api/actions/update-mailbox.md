# Update Mailbox with Woodpecker.co

Updates a mailbox in your Woodpecker account.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/v2/mailboxes/[:smtp_mailbox_id]`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [Update Mailbox](https://developers.woodpecker.co/docs/mailboxes/update-mailbox/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `smtp_mailbox_id` | path | `number` | yes | SMTP mailbox ID from Woodpecker. |
