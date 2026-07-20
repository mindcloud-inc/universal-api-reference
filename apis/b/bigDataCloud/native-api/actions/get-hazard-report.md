# Get Hazard Report with BigDataCloud

Retrieves hazard report details from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/hazard-report`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get Hazard Report](https://www.bigdatacloud.com/ip-geolocation/hazard-report-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | If omitted, BigDataCloud uses the caller IP address. |
