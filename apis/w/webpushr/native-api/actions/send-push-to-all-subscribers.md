# Send Push to All Subscribers with Webpushr

## Endpoint

- **Method:** `POST`
- **Path:** `/notification/send/all`
- **Base URL:** `https://api.webpushr.com/v1`
- **Official documentation:** [Send Push to All Subscribers](https://www.webpushr.com/docs/send-push-to-all-subscribers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `auto_hide` | body | `boolean` | no |
| `expire_push` | body | `string` | no |
| `icon` | body | `string` | no |
| `image` | body | `string` | no |
| `message` | body | `string` | yes |
| `name` | body | `string` | no |
| `send_at` | body | `string` | no |
| `target_url` | body | `string` | yes |
| `title` | body | `string` | yes |
