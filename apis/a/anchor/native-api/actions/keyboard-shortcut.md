# Keyboard Shortcut with Anchor

Sends a keyboard shortcut in an Anchor session.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sessions/:sessionId/keyboard/shortcut`
- **Base URL:** `https://api.anchorbrowser.io`
- **Official documentation:** [Keyboard Shortcut](https://docs.anchorbrowser.io/api-reference/os-level-control/keyboard-shortcut)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `keys[]` | body | `array<string>` | yes |
| `sessionId` | path | `string` | yes |
