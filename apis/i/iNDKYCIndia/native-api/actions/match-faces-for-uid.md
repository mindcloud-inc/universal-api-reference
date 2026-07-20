# Match Faces For UID with IN-D KYC India

Retrieves face match results in IN-D KYC India by UID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/facematch/{uid}`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Match Faces For UID](https://dev.in-d.ai/api-documentation/#operation/facematch_uid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID returned by Generate UID. |
| `image[]` | body | `array<string>` | yes | Two base64-encoded face images to compare. |
