# Initialize Chat with v0

Initializes a new chat in v0 from source content.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chats/init`
- **Base URL:** `https://api.v0.dev`
- **Official documentation:** [Initialize Chat](https://v0.app/docs/api/platform/reference/chats/init)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string` | no |
| `projectId` | body | `string` | no |
| `name` | body | `string` | no |
| `chatPrivacy` | body | `string` | no |
| `metadata` | body | `object` | no |
| `files[]` | body | `array<object>` | no |
| `repo` | body | `object` | no |
| `registry` | body | `object` | no |
| `zip` | body | `object` | no |
| `templateId` | body | `string` | no |
