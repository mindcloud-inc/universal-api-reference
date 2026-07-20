# Create Short Link with lc.cx

Creates a new short link in lc.cx.

## Endpoint

- **Method:** `POST`
- **Path:** `/shorten`
- **Base URL:** `https://api.lc.cx/v1`
- **Official documentation:** [Create Short Link](https://dev.lc.cx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | body | `string` | yes | The destination URL for the new shortlink. |
| `domain` | body | `string` | yes | The domain ID to use for the new shortlink. |
| `custom_path` | body | `string` | no | An optional custom path for the shortlink. |
| `tags[]` | body | `array<string>` | no | Optional tag IDs to attach to the shortlink. |
| `note` | body | `string` | no | An optional note stored on the shortlink. |
| `rule` | body | `string` | no | An optional lc.cx rule value for the shortlink. |
| `expiration_date` | body | `number` | no | An optional UNIX timestamp after which the shortlink expires. |
| `expiration_url` | body | `string` | no | An optional URL to use after the shortlink expires. |
