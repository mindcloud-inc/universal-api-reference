# Delete Ingress with LiveKit

Deletes an existing ingress from LiveKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.Ingress/DeleteIngress`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [Delete Ingress](https://docs.livekit.io/reference/other/ingress/api/#deleteingress)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ingress_id` | body | `string` | yes |
