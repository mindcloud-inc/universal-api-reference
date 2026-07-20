# Update Check with updown.io

Updates an existing check in updown.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/checks/:token`
- **Base URL:** `https://updown.io/api`
- **Official documentation:** [Update Check](https://updown.io/api#PUT-/api/checks/:token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias` | body | `string` | no | Human-readable name for the check. |
| `apdex_t` | body | `number` | no | APDEX threshold in seconds. |
| `custom_headers` | body | `object` | no | Custom HTTP headers for updown requests. |
| `disabled_locations[]` | body | `array<string>` | no | Monitoring locations to disable for this check. |
| `enabled` | body | `boolean` | no | Whether the check is enabled. |
| `http_body` | body | `string` | no | HTTP body sent with the request. |
| `http_verb` | body | `list` | no | HTTP verb used for the check request. Accepted values: `DELETE`, `GET/HEAD`, `OPTIONS`, `PATCH`, `POST`, `PUT`. |
| `mute_until` | body | `string` | no | Mute notifications until the given time, recovery, or forever. |
| `period` | body | `number` | no | Interval in seconds. |
| `published` | body | `boolean` | no | Whether the status page entry is public. |
| `recipients[]` | body | `array<string>` | no | Selected alert recipients for the check. |
| `string_match` | body | `string` | no | Search for this string in the page. |
| `token` | path | `string` | yes | The check unique token. |
| `url` | body | `string` | no | The new URL you want to monitor, except for pulse checks. |
