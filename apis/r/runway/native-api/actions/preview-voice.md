# Preview Voice with Runway

Creates a voice preview in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voices/preview`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Preview Voice](https://docs.dev.runwayml.com/api#tag/Voices/paths/~1v1~1voices~1preview/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Voice design model, such as eleven_multilingual_ttv_v2 or eleven_ttv_v3. |
| `prompt` | body | `string` | yes | Voice description text, at least 20 characters. |
