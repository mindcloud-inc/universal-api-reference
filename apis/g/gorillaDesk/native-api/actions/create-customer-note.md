# Create Customer Note with GorillaDesk

Creates a customer note in GorillaDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/:customerId/notes`
- **Base URL:** `https://api.gorilladesk.com/v1`
- **Official documentation:** [Create Customer Note](https://api.gorilladesk.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments[]` | body | `array<file>` | no | Accepted file types: image, audio, video, pdf. Limit to 5 files and maximum 10MB per file. |
| `content` | body | `string` | yes | — |
| `customerId` | path | `string` | yes | Customer Id |
| `notify_users[]` | body | `array<string>` | no | List of user Ids |
