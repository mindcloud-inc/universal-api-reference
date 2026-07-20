# Match Faces with IN-D KYC India

Retrieves face match results from IN-D KYC India.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/facematch/`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Match Faces](https://dev.in-d.ai/api-documentation/#operation/facematch_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image[]` | body | `array<string>` | yes | Two base64-encoded face images to compare. |
