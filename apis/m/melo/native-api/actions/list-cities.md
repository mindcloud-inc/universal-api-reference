# List Cities with Melo

Retrieves cities from Melo matching the provided criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/cities`
- **Base URL:** `https://preprod-api.notif.immo`
- **Official documentation:** [List Cities](https://docs.melo.io/api-reference/endpoint/indicators/cities)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Collection page number. |
| `name` | query | `string` | no | Filter by city name. |
| `zipcode` | query | `string` | no | Filter by zipcode. |
