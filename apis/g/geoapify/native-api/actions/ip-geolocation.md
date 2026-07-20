# IP Geolocation with Geoapify Geocode

Retrieves IP geolocation data from Geoapify.

## Endpoint

- **Method:** `GET`
- **Path:** `/ipinfo`
- **Base URL:** `https://api.geoapify.com/v1`
- **Official documentation:** [IP Geolocation](https://apidocs.geoapify.com/docs/ip-geolocation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | query | `string` | no | IPv4 or IPv6 address. If omitted, Geoapify uses the caller IP. |
