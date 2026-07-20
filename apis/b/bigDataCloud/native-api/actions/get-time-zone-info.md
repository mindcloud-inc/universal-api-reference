# Get Time Zone Info with BigDataCloud

Retrieves time zone information from BigDataCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/timezone-info`
- **Base URL:** `https://api-bdc.net`
- **Official documentation:** [Get Time Zone Info](https://www.bigdatacloud.com/ip-geolocation/timezone-info-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeZoneId` | query | `string` | no | Time zone name in IANA format. |
| `utcReference` | query | `number` | no | UTC time reference in Unix time seconds. |
