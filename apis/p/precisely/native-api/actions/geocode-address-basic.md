# Geocode Address (Basic) with Precisely

Retrieves geocoding candidates from Precisely for an address.

## Endpoint

- **Method:** `GET`
- **Path:** `/geocode/v1/basic/geocode`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Geocode Address (Basic)](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/Geocode/Geocode/LI_Geo_GET_desc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mainAddress` | query | `string` | yes | Single-line input address, or the street-address portion when structured fields are used. |
| `placeName` | query | `string` | no | Building, place, point of interest, company, or firm name associated with the address. |
| `lastLine` | query | `string` | no | The last line of the address. |
| `areaName1` | query | `string` | no | Largest geographic area, typically a state or province. |
| `areaName3` | query | `string` | no | City or town name. |
| `postalCode` | query | `string` | no | Postal code in the appropriate format for the selected country. |
| `country` | query | `string` | no | ISO country code or country name. |
| `matchMode` | query | `string` | no | Controls how strictly the address is matched. |
| `maxCands` | query | `number` | no | Maximum number of candidates to return. |
| `removeAccentMarks` | query | `boolean` | no | Suppress accents and diacritical marks in the output. |
