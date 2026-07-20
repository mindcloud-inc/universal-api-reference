# Stop Monitoring Vendor with UpGuard

Stops monitoring a vendor in UpGuard.

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/unmonitor`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Stop Monitoring Vendor](https://cyber-risk.upguard.com/api/docs#operation/unmonitorvendor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | query | `string` | no | The hostname of the vendor to stop monitoring when no vendor ID is provided. |
