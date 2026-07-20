# Update Device Fingerprint Postback with IPQS Fraud and Risk Scoring

Updates device fingerprint postback data in IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/postback/{apiKey}`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Update Device Fingerprint Postback](https://www.ipqualityscore.com/documentation/device-fingerprint-api/conversions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | query | `string` | yes | Original device tracker request ID to update. |
| `update[ConversionStatus]` | query | `boolean` | no | Conversion status update value. |
