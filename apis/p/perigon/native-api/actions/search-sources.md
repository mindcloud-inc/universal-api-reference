# Search Sources with Perigon

Finds media sources in Perigon by attributes and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/sources/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search Sources](https://docs.perigon.io/docs/sources-source-groups)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `name` | query | `string` | no | — |
| `sourceGroup` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `sortBy` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `size` | query | `number` | no | — |
| `minMonthlyVisits` | query | `number` | no | — |
| `maxMonthlyVisits` | query | `number` | no | — |
| `country` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `sourceCountry` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `sourceState` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `sourceCity` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `topic` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `label` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `paywall` | query | `boolean` | no | — |
| `showNumResults` | query | `boolean` | no | — |
