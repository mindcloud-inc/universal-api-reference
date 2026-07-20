# Update Short Link with y.gy

Updates an existing short link in y.gy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/link/:id`
- **Base URL:** `https://api.y.gy`
- **Official documentation:** [Update Short Link](https://app.y.gy/docs/api-docs/links)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `add_tags` | body | `list<number>` | no |
| `android_link_destination` | body | `string` | no |
| `bot_protection` | body | `boolean` | no |
| `captcha` | body | `boolean` | no |
| `destination_url` | body | `string` | no |
| `expiration_date` | body | `date` | no |
| `id` | path | `string` | yes |
| `ios_link_destination` | body | `string` | no |
| `name` | body | `string` | no |
| `og_description` | body | `string` | no |
| `og_image` | body | `string` | no |
| `og_title` | body | `string` | no |
| `password` | body | `string` | no |
| `qr_code_background_hex` | body | `string` | no |
| `qr_code_foreground_hex` | body | `string` | no |
| `remove_tags` | body | `list<number>` | no |
| `webhook_auth_key` | body | `string` | no |
| `webhook_url` | body | `string` | no |
