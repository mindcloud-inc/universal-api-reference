# Check Video Liveness For UID with IN-D KYC India

Retrieves video liveness results in IN-D KYC India by UID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/liveliness/{uid}`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Check Video Liveness For UID](https://dev.in-d.ai/api-documentation/#operation/videoliveliness_uid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID returned by Generate UID. |
| `term` | body | `string` | yes | Term or phrase expected in the video liveness check. |
| `video` | body | `string` | yes | Base64-encoded video content. |
| `language` | body | `string` | yes | Language code for the liveness term. |
