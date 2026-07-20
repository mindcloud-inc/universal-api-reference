# Validate ID Number For UID with IN-D KYC India

Retrieves ID number validation results in IN-D KYC India by UID.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/validation/{uid}`
- **Base URL:** `https://api.kyc.in-d.ai`
- **Official documentation:** [Validate ID Number For UID](https://dev.in-d.ai/api-documentation/#operation/validate1_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | UID returned by Generate UID. |
