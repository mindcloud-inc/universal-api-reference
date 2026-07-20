# Type Text with Anchor

Types text in an Anchor session.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sessions/:sessionId/keyboard/type`
- **Base URL:** `https://api.anchorbrowser.io`
- **Official documentation:** [Type Text](https://docs.anchorbrowser.io/api-reference/os-level-control/type-text)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `text` | body | `string` | yes |
