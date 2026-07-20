# Create TCP Ping Measurement with Globalping

Creates a TCP ping measurement in Globalping.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/measurements`
- **Base URL:** `https://api.globalping.io`
- **Official documentation:** [Create TCP Ping Measurement](https://github.com/jsdelivr/globalping#globalping-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | A publicly reachable hostname or IP address to measure. |
| `measurementOptions.port` | body | `number` | no | Destination port for TCP probes. |
