# Search Wikipedia with Perigon

Finds Wikipedia pages through Perigon by text or metadata.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/wikipedia/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search Wikipedia](https://docs.perigon.io/docs/wikipedia)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | — |
| `title` | query | `string` | no | — |
| `category` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `wikidataId` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `wikidataInstanceOfLabel` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `wikiCode` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `pageviewsFrom` | query | `number` | no | — |
| `pageviewsTo` | query | `number` | no | — |
| `withPageviews` | query | `boolean` | no | — |
| `sortBy` | query | `string` | no | — |
| `size` | query | `number` | no | — |
| `page` | query | `number` | no | — |
