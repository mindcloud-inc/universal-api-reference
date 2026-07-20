# Create Paste with Pastefy

## Endpoint

- **Method:** `POST`
- **Path:** `/paste`
- **Base URL:** `https://pastefy.app/api/v2`
- **Official documentation:** [Create Paste](https://docs.pastefy.app/api/spec/post-paste.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ai` | body | `boolean` | no |
| `content` | body | `string` | no |
| `encrypted` | body | `boolean` | no |
| `expireAt` | body | `string` | no |
| `folder` | body | `string` | no |
| `forkedFrom` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
| `title` | body | `string` | no |
| `type` | body | `string` | no |
| `visibility` | body | `string` | no |
