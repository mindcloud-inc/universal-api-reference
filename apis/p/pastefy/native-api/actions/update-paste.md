# Update Paste with Pastefy

## Endpoint

- **Method:** `PUT`
- **Path:** `/paste/:id`
- **Base URL:** `https://pastefy.app/api/v2`
- **Official documentation:** [Update Paste](https://docs.pastefy.app/api/spec/put-paste-%7Bid%7D.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `string` | no |
| `encrypted` | body | `boolean` | no |
| `expireAt` | body | `string` | no |
| `folder` | body | `string` | no |
| `id` | path | `string` | yes |
| `tags[]` | body | `array<string>` | no |
| `title` | body | `string` | no |
| `type` | body | `string` | no |
| `visibility` | body | `string` | no |
