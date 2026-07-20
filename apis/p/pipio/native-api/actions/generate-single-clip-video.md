# Generate Single Clip Video with Pipio

Creates a single-clip video in Pipio.

## Endpoint

- **Method:** `POST`
- **Path:** `https://generate.pipio.ai/single-clip`
- **Base URL:** `https://avatar.pipio.ai`
- **Official documentation:** [Generate Single Clip Video](https://docs.pipio.ai/generate-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actorId` | body | `string` | yes | The unique identifier for your digital actor. |
| `voiceId` | body | `string` | no | The unique identifier for your voice. Only voiceId or language may be sent per request. |
| `language` | body | `string` | no | Language code to apply to the selected avatar. Only language or voiceId may be sent per request. |
| `script` | body | `string` | no | Text script to generate a performance from your digital actor. |
| `audioUrl` | body | `string` | no | URL to an audio file that will be used instead of script-based text to speech. |
| `fps` | body | `number` | no | Frame rate of the video, either 30 or 60. |
| `transparent` | body | `boolean` | no | Whether to render the video with a transparent background. |
| `callbackUrl` | body | `string` | no | Location the server will send the response to. |
