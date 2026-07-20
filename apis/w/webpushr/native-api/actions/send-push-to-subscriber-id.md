# Send Push to Subscriber ID with Webpushr

## Endpoint

- **Method:** `POST`
- **Path:** `/notification/send/sid`
- **Base URL:** `https://api.webpushr.com/v1`
- **Official documentation:** [Send Push to Subscriber ID](https://www.webpushr.com/docs/send-push-to-a-subscriber-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `auto_hide` | body | `boolean` | no |
| `expire_push` | body | `string` | no |
| `icon` | body | `string` | no |
| `message` | body | `string` | yes |
| `name` | body | `string` | no |
| `send_at` | body | `string` | no |
| `sid` | body | `string` | yes |
| `target_url` | body | `string` | yes |
| `title` | body | `string` | yes |
