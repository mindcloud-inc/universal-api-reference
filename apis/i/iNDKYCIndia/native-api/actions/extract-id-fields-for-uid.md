# Extract ID Fields For UID with IN-D KYC India

Retrieves extracted ID fields in IN-D KYC India by UID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/fields/{uid}`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Extract ID Fields For UID](https://dev.in-d.ai/api-documentation/#operation/extract1_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID returned by Generate UID. |
| `filename` | body | `string` | yes | Image file name for the ID document. |
| `payload` | body | `string` | yes | Base64-encoded image content for field extraction. |
