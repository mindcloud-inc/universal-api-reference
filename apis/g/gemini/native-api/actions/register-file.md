# Register File with Gemini

Registers a Cloud Storage file with Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/files:register`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Register File](https://ai.google.dev/api/files#method:-files.register)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uris[]` | body | `array<string>` | yes | Google Cloud Storage URIs to register. |
