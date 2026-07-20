# AI Process Receipt with Encodian - General

Extracts receipt data from a file with Encodian AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AIProcessReceipt`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Process Receipt](https://support.encodian.com/hc/en-gb/articles/18584183726876)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64-encoded source file content. |
