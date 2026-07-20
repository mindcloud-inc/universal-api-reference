# PowerPoint Replace Text with Encodian

Replaces text in PowerPoint files with Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/PowerPoint/PowerPointSearchAndReplaceText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [PowerPoint Replace Text](https://support.encodian.com/hc/en-gb/articles/19804599079836)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | The Base64 encoded content of the source PowerPoint file. |
| `Phrases[]` | body | `array<object>` | yes | Array of phrase objects to locate and replace. Each phrase includes SearchText, optional ReplacementText, matching options, and style overrides. |
| `cultureName` | body | `string` | no | Culture name used when processing the request. |
