# Create Export with HappyScribe

Creates a new export in HappyScribe.

## Endpoint

- **Method:** `POST`
- **Path:** `/exports`
- **Base URL:** `https://www.happyscribe.com/api/v1`
- **Official documentation:** [Create Export](https://dev.happyscribe.com/sections/product/#exports-create-an-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | yes | Export format such as txt, docx, pdf, srt, vtt, json, or fcp. |
| `transcription_ids[]` | body | `array<string>` | yes | One or more transcription IDs to export. |
