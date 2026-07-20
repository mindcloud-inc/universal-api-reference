# Timezone By Location with Precisely

Retrieves time zone details from Precisely by location.

## Endpoint

- **Method:** `GET`
- **Path:** `/timezone/v1/timezone/bylocation`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Timezone By Location](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/TimeZone/Timezone_location/timezone_by_location_get_request.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude in decimal degrees. |
| `longitude` | query | `number` | yes | Longitude in decimal degrees. |
| `timestamp` | query | `number` | yes | Unix timestamp in milliseconds for the moment to evaluate. |
