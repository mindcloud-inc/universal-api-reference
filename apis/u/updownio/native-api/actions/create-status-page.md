# Create Status Page with updown.io

Creates a new status page in updown.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/status_pages`
- **Base URL:** `https://updown.io/api`
- **Official documentation:** [Create Status Page](https://updown.io/api#POST-/api/status-pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_key` | body | `string` | no | Access key for protected pages. |
| `checks[]` | body | `array<string>` | yes | List of check tokens to show on the status page. Send multiple values as a array. |
| `description` | body | `string` | no | Description text displayed below the status page name. |
| `name` | body | `string` | no | Name of the status page. |
| `visibility` | body | `list` | no | Page visibility: public, protected, or private. Accepted values: `private`, `protected`, `public`. |
