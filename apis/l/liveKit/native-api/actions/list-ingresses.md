# List Ingresses with LiveKit

Retrieves ingresses from LiveKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.Ingress/ListIngress`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [List Ingresses](https://docs.livekit.io/reference/other/ingress/api/#listingress)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `room_name` | body | `string` | no |
| `ingress_id` | body | `string` | no |
