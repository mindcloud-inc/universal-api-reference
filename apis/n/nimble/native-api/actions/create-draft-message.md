# Create Draft Message with Nimble

Creates a draft message in Nimble.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/messages/drafts`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Create Draft Message](https://www.nimble.com/developers/docs/#tag/Messages/operation/post-message-draft)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recipients[]` | body | `array<object>` | no |
| `subject` | body | `string` | no |
| `body` | body | `string` | no |
| `sender_credential_id` | body | `string` | no |
