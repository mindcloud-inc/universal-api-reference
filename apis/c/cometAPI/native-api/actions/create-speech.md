# Create Speech with CometAPI

Creates speech audio in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/audio/speech`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Create Speech](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Text to synthesize. |
| `model` | body | `string` | yes | Speech model ID. |
| `voice` | body | `string` | yes | Voice name to use for the audio. |
