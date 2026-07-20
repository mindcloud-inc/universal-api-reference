# Reverse Geocode US Coordinates Including Non Postal Sources with Smarty-streets

Finds nearby US addresses in Smarty-streets by coordinates, including non-postal sources.

## Endpoint

- **Method:** `GET`
- **Path:** `https://us-reverse-geo.api.smarty.com/lookup`
- **Base URL:** `https://us-street.api.smarty.com`
- **Official documentation:** [Reverse Geocode US Coordinates Including Non Postal Sources](https://www.smarty.com/docs/apis/us-reverse-geocoding-api/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude in decimal degrees. |
| `longitude` | query | `number` | yes | Longitude in decimal degrees. |
