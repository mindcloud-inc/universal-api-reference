# Stop Scanning with GSA Site Scanning

Requests a scan device to stop sending scan data.

## Endpoint

- **Method:** `POST`
- **Path:** `/scan/v2/stopscanning`
- **Base URL:** `https://api.sitaflex.aero`
- **Official documentation:** [Stop Scanning](https://www.developer.aero/api-catalog/flex/scan-api-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | body | `string` | yes | Connection ID created for the device on which scanning should stop. |
