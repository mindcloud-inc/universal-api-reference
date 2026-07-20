# Get PreciselyID By Address with Precisely

Retrieves a PreciselyID for an address in Precisely.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/v1/key/byaddress`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Get PreciselyID By Address](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/PreciselyID/byPreciselyID/bypreciselyID.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Single-line address to resolve to a PreciselyID. |
| `country` | query | `string` | no | ISO country code or country name. |
