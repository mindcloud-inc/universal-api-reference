# Create DNS AAAA Measurement with Globalping

Creates a DNS AAAA measurement in Globalping.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/measurements`
- **Base URL:** `https://api.globalping.io`
- **Official documentation:** [Create DNS AAAA Measurement](https://github.com/jsdelivr/globalping#globalping-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | Hostname to resolve. |
| `limit` | body | `number` | no | Maximum number of probes to run. |
