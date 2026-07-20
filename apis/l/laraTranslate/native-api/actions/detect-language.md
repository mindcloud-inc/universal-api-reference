# Detect language with Lara Translate

Detects the source language of text in Lara Translate.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://mcp-v2.laratranslate.com/v1`
- **Official documentation:** [Detect language](https://developers.laratranslate.com/docs/getting-started-with-mcp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | Text to detect language for. |
| `hint` | body | `string` | no | Optional language hint to guide detection. |
| `passlist[]` | body | `array<string>` | no | Optional list of allowed language codes. |
