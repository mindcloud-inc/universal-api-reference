# Voice Isolation with Runway

Creates a voice isolation task in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice_isolation`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Voice Isolation](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1voice_isolation/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audioUri` | body | `string` | yes | HTTPS URL, Runway URI, or data URI for the source audio. |
| `model` | body | `string` | yes | Runway currently requires eleven_voice_isolation. |
