# Create Ingress with LiveKit

Creates a new ingress in LiveKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.Ingress/CreateIngress`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [Create Ingress](https://docs.livekit.io/reference/other/ingress/api/#createingress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input_type` | body | `string` | yes | Ingress input type, such as RTMP_INPUT, WHIP_INPUT, or URL_INPUT. |
| `name` | body | `string` | no | — |
| `room_name` | body | `string` | yes | — |
| `participant_identity` | body | `string` | yes | — |
| `participant_name` | body | `string` | no | — |
| `enable_transcoding` | body | `boolean` | no | For RTMP_INPUT, LiveKit requires transcoding to be enabled. Set false only for input types/configurations that support bypassing transcoding. |
| `url` | body | `string` | no | HTTP, HLS, MP4, MOV, MKV, OGG, MP3, M4A, or SRT URL for URL_INPUT ingress. |
