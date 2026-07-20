# Create IPv6 Ping Measurement with Globalping

Creates an IPv6 ping measurement in Globalping.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/measurements`
- **Base URL:** `https://api.globalping.io`
- **Official documentation:** [Create IPv6 Ping Measurement](https://github.com/jsdelivr/globalping#globalping-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | A publicly reachable hostname to measure over IPv6. |
| `limit` | body | `number` | no | Maximum number of probes to run. |
