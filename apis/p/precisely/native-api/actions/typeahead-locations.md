# Typeahead Locations with Precisely

Finds address suggestions in Precisely by partial location input.

## Endpoint

- **Method:** `GET`
- **Path:** `/typeahead/v1/locations`
- **Base URL:** `https://api.precisely.com`
- **Official documentation:** [Typeahead Locations](https://docs.precisely.com/docs/sftw/precisely-apis/main/en-us/webhelp/apis/AddressAutocomplete/addressautocomplete_desc.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchText` | query | `string` | yes | The partial address text to search for. |
| `country` | query | `string` | no | ISO country code to search within. |
| `latitude` | query | `number` | no | The latitude of the reference location. |
| `longitude` | query | `number` | no | The longitude of the reference location. |
| `ipAddress` | query | `string` | no | IP address used to detect a search location when coordinates are not supplied. |
| `areaName1` | query | `string` | no | Largest geographic area, typically a state or province. |
| `areaName3` | query | `string` | no | City or town name used with country filtering. |
| `postCode` | query | `string` | no | Postal code used with country filtering. |
| `maxCandidates` | query | `number` | no | Maximum number of address suggestions to return. |
| `searchRadius` | query | `number` | no | Radius to search within around the reference location. |
| `searchRadiusUnit` | query | `string` | no | Unit for the search radius. |
| `autoDetectLocation` | query | `string` | no | Whether to auto-detect location from the IP address. |
| `returnAdminAreasOnly` | query | `string` | no | Whether to return only admin-area matches. |
| `searchOnAddressNumber` | query | `string` | no | Whether to prefer matching on address number. |
| `includeRangesDetails` | query | `string` | no | Whether to include ranges and unit details in the response. |
| `searchOnUnitInfo` | query | `string` | no | Whether to search unit information such as apartment or house number. |
| `searchOnPOBox` | query | `string` | no | Whether to include PO Box matches in the search. |
