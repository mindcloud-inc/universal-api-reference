# Send email via Mumara with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/mumara/send-email`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Send email via Mumara](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient` | body | `string` | yes | Recipient email address |
| `subject` | body | `string` | yes | Email subject |
| `body` | body | `string` | yes | HTML or plain text email body |
| `from_name` | body | `string` | no | Sender name (optional, falls back to user settings) |
| `from_email` | body | `string` | no | Sender email (optional, uses domain/node settings) |
| `reply_to` | body | `string` | no | Reply-to address (optional) |
| `nodeId` | body | `string` | no | Optional - Specific sending node ID (DynamoDB UUID) |
| `domainId` | body | `string` | no | Optional - Specific domain ID (DynamoDB UUID) |
