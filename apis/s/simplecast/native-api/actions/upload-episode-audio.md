# Upload Episode Audio with Simplecast

Uploads episode audio to Simplecast.

## Endpoint

- **Method:** `POST`
- **Path:** `/episodes/:episode_id/audio`
- **Base URL:** `https://api.simplecast.com`
- **Official documentation:** [Upload Episode Audio](https://apidocs.simplecast.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | Publicly reachable audio file URL to attach to the episode. |
| `episode_id` | path | `string` | yes | Simplecast episode identifier. |
