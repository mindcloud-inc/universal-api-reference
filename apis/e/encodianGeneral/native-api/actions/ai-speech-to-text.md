# AI Speech To Text with Encodian - General

Transcribes speech from an audio file in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/AISpeechToText`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [AI Speech To Text](https://support.encodian.com/hc/en-gb/articles/15851898717340)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64-encoded audio file content. |
