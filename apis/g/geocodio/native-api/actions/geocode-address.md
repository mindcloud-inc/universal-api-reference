# Geocode Address with Geocodio

Retrieves geocoding results from Geocodio for one address.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Geocode Address](https://www.geocod.io/docs/#single-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | The address, city, ZIP/postal code, or stable address key to geocode. |
| `country` | query | `string` | no | Optional country to geocode in. Supported values are USA, Canada, or Mexico. |
| `fields` | query | `string` | no | Optional comma-separated list of data append fields, such as timezone, cd, census, zip4, or acs-demographics. Send multiple values as a string separated by `,`. |
| `limit` | query | `number` | no | Optional maximum number of geocoding results to return. |
| `format` | query | `string` | no | Optional response format. Geocodio currently documents simple as the alternate format. Accepted values: `0`. |
