# Replace Sender with UseINBOX

Replaces an existing sender in UseINBOX.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inbox/v1/senders/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Replace Sender](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Sender ID from INBOX. |
| `DisplayName` | body | `string` | yes | Sender display name. |
| `Email` | body | `string` | yes | Sender email address. |
| `ReplyEmail` | body | `string` | yes | Reply-to email address. |
