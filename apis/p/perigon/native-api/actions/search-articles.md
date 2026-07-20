# Search Articles with Perigon

Finds news articles in Perigon by keywords and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/articles/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search Articles](https://docs.perigon.io/docs/overview)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | — |
| `articleId` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `clusterId` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `sortBy` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `size` | query | `number` | no | — |
| `from` | query | `date` | no | — |
| `to` | query | `date` | no | — |
| `source` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `sourceGroup` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `language` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `topic` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `country` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `journalistId` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `companyName` | query | `string` | no | — |
| `showNumResults` | query | `boolean` | no | — |
| `showReprints` | query | `boolean` | no | — |
