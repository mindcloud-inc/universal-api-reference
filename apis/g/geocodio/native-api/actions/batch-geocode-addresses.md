# Batch Geocode Addresses with Geocodio

Retrieves geocoding results from Geocodio for multiple addresses.

## Endpoint

- **Method:** `POST`
- **Path:** `/geocode`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Batch Geocode Addresses](https://www.geocod.io/docs/#batch-geocoding)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload[]` | body | `array<string>` | yes | Array or keyed object of addresses to geocode. |
| `fields` | query | `string` | no | Optional comma-separated list of data append fields. Send multiple values as a string separated by `,`. |
| `limit` | query | `number` | no | Optional maximum number of results per address. |
