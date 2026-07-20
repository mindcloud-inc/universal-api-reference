# Create Traceroute Measurement with Globalping

Creates a traceroute measurement in Globalping.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/measurements`
- **Base URL:** `https://api.globalping.io`
- **Official documentation:** [Create Traceroute Measurement](https://github.com/jsdelivr/globalping#globalping-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | A publicly reachable hostname or IP address to measure. |
| `limit` | body | `number` | no | Maximum number of probes to run. |
