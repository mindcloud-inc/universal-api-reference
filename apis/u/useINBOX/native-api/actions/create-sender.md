# Create Sender with UseINBOX

Creates a sender in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/senders`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Create Sender](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DisplayName` | body | `string` | yes | Sender display name. |
| `Email` | body | `string` | yes | Sender email address. |
| `ReplyEmail` | body | `string` | yes | Reply-to email address. |
