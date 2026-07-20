# Update webhook with Good Grants

Updates an existing webhook in Good Grants.

## Endpoint

- **Method:** `PUT`
- **Path:** `webhook/:slug`
- **Base URL:** `https://api.cr4ce.com`
- **Official documentation:** [Update webhook](https://apidocs.goodgrants.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Webhook slug |
| `method` | body | `string` | no | Webhook HTTP method |
| `name` | body | `string` | no | Webhook name |
| `signing_key` | body | `string` | no | Signing key |
| `url` | body | `string` | no | Webhook URL |
| `events[]` | body | `array<string>` | no | Webhook events |
