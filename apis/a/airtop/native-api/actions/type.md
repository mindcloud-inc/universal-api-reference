# Type with Airtop

Types text in a specific Airtop window.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/type`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Type](https://docs.airtop.ai/api-reference/airtop-api/windows/type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | — |
| `windowId` | path | `string` | yes | — |
| `text` | body | `string` | yes | The text to type into the browser window |
| `elementDescription` | body | `string` | no | Where to type, described in natural language |
| `clearInputField` | body | `boolean` | no | — |
| `pressEnterKey` | body | `boolean` | no | — |
