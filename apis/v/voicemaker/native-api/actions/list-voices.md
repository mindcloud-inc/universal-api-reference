# List Voices with Voicemaker

Retrieves all available voices from Voicemaker.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/voice/list`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [List Voices](https://developer.voicemaker.in/apidocs/list-of-all-voices)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | body | `string` | yes | Language code used to filter available voices, for example en-US. |
