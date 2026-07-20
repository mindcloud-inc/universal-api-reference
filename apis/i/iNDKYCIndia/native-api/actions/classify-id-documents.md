# Classify ID Documents with IN-D KYC India

Retrieves ID document classifications from IN-D KYC India.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/class/`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Classify ID Documents](https://dev.in-d.ai/api-documentation/#operation/classify_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Image file name for the ID document. |
| `payload` | body | `string` | yes | Base64-encoded image content for the ID document. |
