# AI Process Contract with Encodian - General

Extracts contract data from a file with Encodian AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AIProcessContract`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Process Contract](https://support.encodian.com/hc/en-gb/articles/18583890798620)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64-encoded source file content. |
