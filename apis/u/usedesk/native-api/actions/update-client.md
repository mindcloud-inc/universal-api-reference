# Update Client with Usedesk

Updates an existing client in Usedesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/update/client`
- **Base URL:** `https://secure.usedesk.com/uapi`
- **Official documentation:** [Update Client](https://api.usedocs.com/article/51386)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | yes | Client ID. |
| `name` | body | `string` | no | New client name. |
| `phone` | body | `string` | no | Client phone number to add. |
| `emails[]` | body | `array<string>` | no | Email addresses to add to the client. |
