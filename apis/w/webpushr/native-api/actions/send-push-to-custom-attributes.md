# Send Push to Custom Attributes with Webpushr

## Endpoint

- **Method:** `POST`
- **Path:** `/notification/send/attribute`
- **Base URL:** `https://api.webpushr.com/v1`
- **Official documentation:** [Send Push to Custom Attributes](https://www.webpushr.com/docs/send-push-to-a-custom-attribute)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `attribute` | body | `object` | yes |
| `auto_hide` | body | `boolean` | no |
| `expire_push` | body | `string` | no |
| `icon` | body | `string` | no |
| `message` | body | `string` | yes |
| `name` | body | `string` | no |
| `send_at` | body | `string` | no |
| `target_url` | body | `string` | yes |
| `title` | body | `string` | yes |
