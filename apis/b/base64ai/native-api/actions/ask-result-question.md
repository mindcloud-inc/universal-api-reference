# Ask Result Question with Base64.ai

Retrieves answers to questions about a Base64.ai result.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/result/ask/:resultUuid`
- **Base URL:** `https://base64.ai`
- **Official documentation:** [Ask Result Question](https://apidoc.base64.ai/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resultUuid` | path | `string` | yes | Base64.ai result UUID. |
| `questions[]` | body | `array<string>` | yes | One or more natural-language questions about the result. |
