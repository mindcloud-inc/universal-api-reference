# Update Ingress with LiveKit

Updates an existing ingress in LiveKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.Ingress/UpdateIngress`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [Update Ingress](https://docs.livekit.io/reference/other/ingress/api/#updateingress)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ingress_id` | body | `string` | yes |
| `name` | body | `string` | no |
| `room_name` | body | `string` | no |
| `participant_identity` | body | `string` | no |
| `participant_name` | body | `string` | no |
