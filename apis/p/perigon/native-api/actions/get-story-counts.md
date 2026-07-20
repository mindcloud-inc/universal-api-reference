# Get Story Counts with Perigon

Retrieves Perigon story counts grouped by filters or dimensions.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/stories/stats`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Get Story Counts](https://docs.perigon.io/docs/stories-overview)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `splitBy` | query | `string` | yes | — |
| `q` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `size` | query | `number` | no | — |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `topic` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `source` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `country` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `personName` | query | `string` | no | — |
| `companyName` | query | `string` | no | — |
| `showNumResults` | query | `boolean` | no | — |
| `expandArticles` | query | `boolean` | no | — |
