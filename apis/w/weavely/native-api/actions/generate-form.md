# Generate Form with Weavely

Creates a generated form in Weavely from a prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/generate`
- **Base URL:** `https://api.weavely.ai/v1`
- **Official documentation:** [Generate Form](https://help.weavely.ai/developers/forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | A friendly name for the form. |
| `prompt` | body | `string` | yes | A natural-language description of the form to generate. |
| `files[]` | body | `array<object>` | no | Optional files as an array of objects with mimeType and base64-encoded data. |
