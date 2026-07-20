# Timezone By Address with Precisely

Retrieves time zone details from Precisely by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/timezone/v1/timezone/byaddress`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Timezone By Address](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/TimeZone/Timezone_address/timezone_by_address_get_request.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Single-line address to resolve to a timezone. |
| `timestamp` | query | `number` | yes | Unix timestamp in milliseconds for the moment to evaluate. |
