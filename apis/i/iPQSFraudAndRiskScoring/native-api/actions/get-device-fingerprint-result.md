# Get Device Fingerprint Result with IPQS Fraud and Risk Scoring

Retrieves device fingerprint verification results from IPQS.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.ipqualityscore.com/api/tracker/results/{apiKey}/:ip/:deviceId`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Get Device Fingerprint Result](https://www.ipqualityscore.com/documentation/device-fingerprint-api/verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | End-user IP address associated with the device ID. |
| `deviceId` | path | `string` | yes | Device fingerprint ID returned by the IPQS tracker. |
