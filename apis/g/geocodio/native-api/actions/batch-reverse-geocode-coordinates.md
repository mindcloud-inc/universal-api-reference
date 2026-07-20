# Batch Reverse Geocode Coordinates with Geocodio

Retrieves address details from Geocodio for multiple coordinates.

## Endpoint

- **Method:** `POST`
- **Path:** `/reverse`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Batch Reverse Geocode Coordinates](https://www.geocod.io/docs/#batch-reverse-geocoding)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload[]` | body | `array<string>` | yes | Array or keyed object of coordinates to reverse geocode. |
| `fields` | query | `string` | no | Optional comma-separated list of data append fields. Send multiple values as a string separated by `,`. |
| `skipGeocoding` | query | `boolean` | no | When present, extracts field data from coordinates without reverse geocoding. |
