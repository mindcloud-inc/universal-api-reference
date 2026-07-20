# Navigate to URL with Anchor

Navigates an Anchor session to a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sessions/:sessionId/goto`
- **Base URL:** `https://api.anchorbrowser.io`
- **Official documentation:** [Navigate to URL](https://docs.anchorbrowser.io/api-reference/os-level-control/navigate-to-url)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `url` | body | `string` | yes |
