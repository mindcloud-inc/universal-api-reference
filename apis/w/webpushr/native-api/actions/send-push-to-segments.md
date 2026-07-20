# Send Push to Segments with Webpushr

## Endpoint

- **Method:** `POST`
- **Path:** `/notification/send/segment`
- **Base URL:** `https://api.webpushr.com/v1`
- **Official documentation:** [Send Push to Segments](https://www.webpushr.com/docs/send-push-to-a-segment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `auto_hide` | body | `boolean` | no |
| `expire_push` | body | `string` | no |
| `icon` | body | `string` | no |
| `image` | body | `string` | no |
| `message` | body | `string` | yes |
| `name` | body | `string` | no |
| `segment[]` | body | `array<number>` | yes |
| `send_at` | body | `string` | no |
| `target_url` | body | `string` | yes |
| `title` | body | `string` | yes |
