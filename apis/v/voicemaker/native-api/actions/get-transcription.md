# Get Transcription with Voicemaker

Retrieves a single transcription from Voicemaker.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/speech-to-text/{taskId}`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [Get Transcription](https://developer.voicemaker.in/apidocs/get-single-transcription-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | Transcription task ID to retrieve. |
