# Update Sender with UseINBOX

Updates an existing sender in UseINBOX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inbox/v1/senders/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Update Sender](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Sender ID from INBOX. |
| `DisplayName` | body | `string` | no | Updated sender display name. |
