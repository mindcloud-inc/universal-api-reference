# Create UDP MTR Measurement with Globalping

Creates a UDP MTR measurement in Globalping.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/measurements`
- **Base URL:** `https://api.globalping.io`
- **Official documentation:** [Create UDP MTR Measurement](https://github.com/jsdelivr/globalping#globalping-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | A publicly reachable hostname or IP address to measure. |
| `measurementOptions.port` | body | `number` | no | Destination port for UDP probes. |
