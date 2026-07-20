# Create Recording (Text-to-Speech) with DialMyCalls

Creates a text-to-speech recording in DialMyCalls.

## Endpoint

- **Method:** `POST`
- **Path:** `/recording/tts`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Create Recording (Text-to-Speech)](https://www.dialmycalls.com/api-documentation#recording-create-tts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gender` | body | `string` | yes | Gender of the recording. Options: M or F. |
| `language` | body | `string` | yes | Language of the recording. Options: en or es. |
| `name` | body | `string` | yes | The name of the recording. |
| `text` | body | `string` | yes | The text to convert to speech. |
