# Classify ID Documents For UID with IN-D KYC India

Retrieves ID document classifications in IN-D KYC India by UID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/class/{uid}`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Classify ID Documents For UID](https://dev.in-d.ai/api-documentation/#operation/classify1_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID returned by Generate UID. |
| `filename` | body | `string` | yes | Image file name for the ID document. |
| `payload` | body | `string` | yes | Base64-encoded image content for the ID document. |
