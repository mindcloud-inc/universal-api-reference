# Get Time Zone by Location with BigDataCloud

Retrieves time zone details by location from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/timezone-by-location`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get Time Zone by Location](https://www.bigdatacloud.com/reverse-geocoding/timezone-by-location-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | no | Latitude value in the WGS 84 reference system. |
| `longitude` | query | `number` | no | Longitude value in the WGS 84 reference system. |
| `utcReference` | query | `number` | no | UTC time reference in Unix time seconds. |
