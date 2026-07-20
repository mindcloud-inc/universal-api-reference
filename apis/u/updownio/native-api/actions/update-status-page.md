# Update Status Page with updown.io

Updates an existing status page in updown.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/status_pages/:token`
- **Base URL:** `https://updown.io/api`
- **Official documentation:** [Update Status Page](https://updown.io/api#PUT-/api/status-pages/:token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_key` | body | `string` | no | Access key for protected pages. |
| `checks[]` | body | `array<string>` | no | List of check tokens to show on the status page. Send multiple values as a array. |
| `description` | body | `string` | no | Description text displayed below the status page name. |
| `name` | body | `string` | no | Name of the status page. |
| `token` | path | `string` | yes | The status page unique token. |
| `visibility` | body | `list` | no | Page visibility: public, protected, or private. Accepted values: `private`, `protected`, `public`. |
