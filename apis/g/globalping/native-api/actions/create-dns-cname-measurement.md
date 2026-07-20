# Create DNS CNAME Measurement with Globalping

Creates a DNS CNAME measurement in Globalping.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/measurements`
- **Base URL:** `https://api.globalping.io`
- **Official documentation:** [Create DNS CNAME Measurement](https://github.com/jsdelivr/globalping#globalping-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | Hostname to resolve. |
