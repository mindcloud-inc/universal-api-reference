# Suggest what3words Addresses with What3Words

Finds suggested what3words addresses from text input.

## Endpoint

- **Method:** `GET`
- **Path:** `/autosuggest`
- **Base URL:** `https://api.what3words.com/v3`
- **Official documentation:** [Suggest what3words Addresses](https://developer.what3words.com/public-api/docs#autosuggest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | query | `string` | yes | Full or partial what3words address. At minimum, use the first two complete words plus one character from the third word. |
| `focus` | query | `string` | no | Latitude and longitude used to prioritize nearby suggestions, for example 51.521251,-0.203586. |
| `n-results` | query | `number` | no | Number of suggestions to return. Values over 100 are truncated to 100. |
| `n-focus-results` | query | `number` | no | Number of top suggestions strongly biased toward the focus coordinate. |
| `clip-to-country` | query | `string` | no | Restrict suggestions to comma-separated ISO 3166-1 alpha-2 country codes, for example GB,US. |
| `clip-to-circle` | query | `string` | no | Restrict suggestions to latitude,longitude,kilometres, for example 51.4243877,-0.3474524,10. |
| `clip-to-bounding-box` | query | `string` | no | Restrict suggestions to southwest latitude, southwest longitude, northeast latitude, northeast longitude. |
| `clip-to-polygon` | query | `string` | no | Restrict suggestions to a closed polygon of comma-separated latitude/longitude pairs, up to 25 pairs. |
| `language` | query | `string` | no | Preferred language or locale to guide autosuggest. Required for voice input modes. |
| `locale` | query | `string` | no | Optional locale or script-specific code. If language is also provided, both values must match. |
| `input-type` | query | `list<string>` | no | Input mode. Text is the default; voice modes require language. Accepted values: `generic-voice`, `nmdp-asr`, `speechmatics`, `text`, `vin-big-data`, `vocon-hybrid`. |
| `prefer-land` | query | `boolean` | no | Prefer land-based suggestions. Enabled by default by what3words. |
| `format` | query | `list<string>` | no | Response format: json or geojson. Accepted values: `geojson`, `json`. |
