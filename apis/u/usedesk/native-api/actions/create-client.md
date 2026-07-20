# Create Client with Usedesk

Creates a new client in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/create/client`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Create Client](https://api.usedocs.com/article/51385)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | New customer name. |
| `note` | body | `string` | no | Client note text. |
| `phone` | body | `string` | no | Client phone number. |
| `emails[]` | body | `array<string>` | no | Email addresses for the new client. |
