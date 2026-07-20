# Check Face Liveness with IN-D KYC India

Retrieves face liveness results from IN-D KYC India.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/facelivenessv2/`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Check Face Liveness](https://dev.in-d.ai/api-documentation/#operation/faceliveness_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Base64-encoded face image content. |
