# Create Short Link with y.gy

Creates a new short link in y.gy.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/link`
- **Base URL:** `https://api.y.gy`
- **Official documentation:** [Create Short Link](https://app.y.gy/docs/api-docs/links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `android_link_destination` | body | `string` | no | — |
| `destination_url` | body | `string` | yes | The short link redirects to this URL. |
| `disable_png` | query | `boolean` | no | Disable PNG QR generation and return only SVG. |
| `domain` | body | `string` | no | Use a verified custom domain or omit to use y.gy. |
| `expiration_date` | body | `date` | no | — |
| `ios_link_destination` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `og_description` | body | `string` | no | — |
| `og_image` | body | `string` | no | — |
| `og_title` | body | `string` | no | — |
| `password` | body | `string` | no | — |
| `qr_code_background_hex` | body | `string` | no | — |
| `qr_code_foreground_hex` | body | `string` | no | — |
| `suffix` | body | `string` | no | — |
| `tags` | body | `list<number>` | no | — |
| `webhook_auth_key` | body | `string` | no | — |
| `webhook_url` | body | `string` | no | — |
