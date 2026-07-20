# Create Live Job with Gladia

Creates a live transcription job in Gladia.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/live`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Create Live Job](https://docs.gladia.io/api-reference/v2/live/init)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `encoding` | body | `string` | no | Audio encoding for the live stream. Match this to the audio chunks sent over the WebSocket. |
| `sample_rate` | body | `number` | no | Sample rate in Hz for the live audio stream. |
| `bit_depth` | body | `number` | no | Bit depth for the live audio stream. |
| `channels` | body | `number` | no | Channel count for the live audio stream. |
| `region` | query | `list<string>` | no | Optional region used to process the live audio stream. Accepted values: `0`, `1`. |
