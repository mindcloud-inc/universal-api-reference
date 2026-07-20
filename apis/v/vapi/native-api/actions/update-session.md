# Update Session with Vapi

Updates an existing session in Vapi.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/session/:id`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Update Session](https://docs.vapi.ai/api-reference/sessions/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | This is the new name for the session. Maximum length is 40 characters. |
| `status` | body | `string` | no | This is the new status for the session. |
| `expirationSeconds` | body | `number` | no | Session expiration time in seconds. Defaults to 24 hours (86400 seconds) if not set. |
| `messages[]` | body | `array<object>` | no | This is the updated array of chat messages. |
