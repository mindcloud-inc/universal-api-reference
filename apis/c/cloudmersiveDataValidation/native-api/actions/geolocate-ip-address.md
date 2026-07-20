# Geolocate IP Address with Cloudmersive Data Validation

Geolocates an IP address with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/ip/geolocate`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Geolocate IP Address](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `value` | body | `string` | yes | IP address to geolocate. |
