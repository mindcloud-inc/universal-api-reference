# Get User Risk with BigDataCloud

Retrieves user risk details from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/user-risk`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get User Risk](https://www.bigdatacloud.com/ip-geolocation/user-risk-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | If omitted, BigDataCloud uses the caller IP address. |
