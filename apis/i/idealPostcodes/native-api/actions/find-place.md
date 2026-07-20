# Find Place with Ideal Postcodes

Finds place suggestions in Ideal Postcodes by text query.

## Endpoint

- **Method:** `GET`
- **Path:** `/places`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Find Place](https://docs.ideal-postcodes.co.uk/docs/api/find-place)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Place query string. |
| `country_iso` | query | `string` | no | Comma-separated ISO 3166-1 alpha-3 country codes to filter by. |
| `bias_country_iso` | query | `string` | no | Comma-separated ISO 3166-1 alpha-3 country codes to bias results toward. |
| `bias_lonlat` | query | `string` | no | Longitude, latitude, and radius bias in the form lon,lat,radius. |
| `bias_ip` | query | `boolean` | no | Set to true to bias results using the request IP location. |
