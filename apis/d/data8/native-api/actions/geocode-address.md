# Geocode Address with Data8

Geocodes a submitted address with Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/Location/Geocode.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Geocode Address](https://docs.data-8.co.uk/web-services/geocoding/geocode)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `name` | body | `string` | yes | The address or place name to geocode. |
| `options` | body | `object` | no | Optional settings that control geocoding behavior. |
