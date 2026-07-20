# List Organizations with Pledge

Retrieves organizations from Pledge.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [List Organizations](https://developer.pledge.to/api/#tag/Organizations/operation/getAllOrganizations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Keyword search on name, alias, or mission. |
| `ngo_id` | query | `string` | no | Filter by NGO ID. |
| `cause_id` | query | `number` | no | Filter by cause ID. |
| `country` | query | `string` | no | Filter by ISO 3166-1 alpha-2 country code. |
| `region` | query | `string` | no | Filter by region. |
| `postal_code` | query | `string` | no | Filter by postal or zip code. |
| `lat` | query | `string` | no | Latitude for proximity search. Must be paired with longitude. |
| `lon` | query | `string` | no | Longitude for proximity search. Must be paired with latitude. |
