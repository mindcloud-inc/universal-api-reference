# Create Template with Sakari SMS

Creates a new template in Sakari SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/templates`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Create Template](https://developer.sakari.io/api-reference/templates/create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `template` | body | `string` | no | — |
| `media[]` | body | `array<object>` | no | List of media objects attached to message |
| `media.media[].url` | body | `string` | no | — |
| `media.media[].type` | body | `string` | no | — |
| `media.media[].name` | body | `string` | no | — |
| `media.media[].filename` | body | `string` | no | — |
