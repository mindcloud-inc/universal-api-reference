# Extract ID Fields with IN-D KYC India

Retrieves extracted ID fields from IN-D KYC India.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/fields/`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Extract ID Fields](https://dev.in-d.ai/api-documentation/#operation/extract_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | Image file name for the ID document. |
| `payload` | body | `string` | yes | Base64-encoded image content for field extraction. |
