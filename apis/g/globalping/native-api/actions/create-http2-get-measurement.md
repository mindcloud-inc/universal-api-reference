# Create HTTP2 GET Measurement with Globalping

Creates an HTTP2 GET measurement in Globalping.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/measurements`
- **Base URL:** `https://api.globalping.io`
- **Official documentation:** [Create HTTP2 GET Measurement](https://github.com/jsdelivr/globalping#globalping-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | Hostname or URL host to request. |
