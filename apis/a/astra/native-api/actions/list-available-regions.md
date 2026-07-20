# List Available Regions with Astra

Retrieves available Astra serverless regions.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/regions/serverless`
- **Base URL:** `https://api.astra.datastax.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter-by-org` | query | `boolean` | no | When true, return only regions enabled for the caller organization. |
| `region-type` | query | `string` | no | Optional region type filter such as all or vector. |
