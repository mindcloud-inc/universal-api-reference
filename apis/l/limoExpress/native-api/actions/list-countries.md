# List Countries with LimoExpress

Retrieves countries from the LimoExpress platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/countries`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List Countries](https://api.limoexpress.me/api/docs/v1#/Countries/getAllCountries)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Search across country fields. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
