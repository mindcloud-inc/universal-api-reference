# Create webhook with Good Grants

Creates a new webhook in Good Grants.

## Endpoint

- **Method:** `POST`
- **Path:** `webhook`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [Create webhook](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `method` | body | `string` | yes | Webhook HTTP method |
| `name` | body | `string` | yes | Webhook name |
| `signing_key` | body | `string` | no | Signing key |
| `url` | body | `string` | yes | Webhook URL |
| `events[]` | body | `array<string>` | yes | Webhook events |
