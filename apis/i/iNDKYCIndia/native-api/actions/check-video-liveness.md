# Check Video Liveness with IN-D KYC India

Retrieves video liveness results from IN-D KYC India.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/liveliness/`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Check Video Liveness](https://dev.in-d.ai/api-documentation/#operation/videoliveliness_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | body | `string` | yes | Term or phrase expected in the video liveness check. |
| `video` | body | `string` | yes | Base64-encoded video content. |
| `language` | body | `string` | yes | Language code for the liveness term. |
