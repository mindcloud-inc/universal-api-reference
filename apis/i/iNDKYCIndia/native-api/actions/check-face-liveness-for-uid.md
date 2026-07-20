# Check Face Liveness For UID with IN-D KYC India

Retrieves face liveness results in IN-D KYC India by UID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/facelivenessv2/{uid}`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Check Face Liveness For UID](https://dev.in-d.ai/api-documentation/#operation/faceliveness_uid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID returned by Generate UID. |
| `image` | body | `string` | yes | Base64-encoded face image content. |
