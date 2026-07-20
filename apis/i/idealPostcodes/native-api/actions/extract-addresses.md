# Extract Addresses with Ideal Postcodes

Finds addresses in Ideal Postcodes by text query.

## Endpoint

- **Method:** `GET`
- **Path:** `/addresses`
- **Base URL:** `https://api.ideal-postcodes.co.uk/v1`
- **Official documentation:** [Extract Addresses](https://docs.ideal-postcodes.co.uk/docs/api/addresses)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Address text to query. |
| `filter` | query | `string` | no | Comma-separated whitelist of response fields to return. |
| `lon` | query | `number` | no | Longitude for reverse geocoding; use together with latitude. |
| `lat` | query | `number` | no | Latitude for reverse geocoding; use together with longitude. |
| `postcode_outward` | query | `string` | no | Filter results by outward postcode code. |
| `postcode` | query | `string` | no | Filter results by postcode. |
| `postcode_area` | query | `string` | no | Filter results by postcode area. |
| `postcode_sector` | query | `string` | no | Filter results by postcode sector. |
| `post_town` | query | `string` | no | Filter results by town or city. |
| `uprn` | query | `number` | no | Filter results by UPRN. |
| `country` | query | `string` | no | Filter results by country name. |
| `postcode_type` | query | `string` | no | Filter results by postcode type. |
| `su_organisation_indicator` | query | `string` | no | Filter results by organisation indicator. |
| `box` | query | `string` | no | Restrict search to a bounding box. |
| `bias_postcode_outward` | query | `string` | no | Bias results toward a matching outward code. |
| `bias_postcode` | query | `string` | no | Bias results toward a matching postcode. |
| `bias_postcode_area` | query | `string` | no | Bias results toward a matching postcode area. |
| `bias_postcode_sector` | query | `string` | no | Bias results toward a matching postcode sector. |
| `bias_post_town` | query | `string` | no | Bias results toward a matching town or city. |
| `bias_thoroughfare` | query | `string` | no | Bias results toward a street or thoroughfare. |
| `bias_country` | query | `string` | no | Bias results toward a matching country. |
| `bias_lonlat` | query | `string` | no | Bias using longitude, latitude, and radius in meters. |
| `tags` | query | `string` | no | Comma-separated tags used to annotate the request context. |
