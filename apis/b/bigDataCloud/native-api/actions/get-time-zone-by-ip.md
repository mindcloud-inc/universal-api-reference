# Get Time Zone by IP with BigDataCloud

Retrieves time zone details by IP address from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/timezone-by-ip`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get Time Zone by IP](https://www.bigdatacloud.com/ip-geolocation/timezone-by-ip-address-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | If omitted, BigDataCloud uses the caller IP address. |
| `utcReference` | query | `number` | no | UTC time reference in Unix time seconds. |
