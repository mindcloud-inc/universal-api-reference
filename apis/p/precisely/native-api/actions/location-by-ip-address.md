# Location By IP Address with Precisely

Retrieves location coordinates from Precisely by IP address.

## Endpoint

- **Method:** `GET`
- **Path:** `/geolocation/v1/location/byipaddress`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Location By IP Address](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geolocation/location_by_ip_address.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddress` | query | `string` | yes | Public IPv4 or IPv6 address to geolocate. |
