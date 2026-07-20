# Search Journalists with Perigon

Finds journalists in Perigon by name, source, or topic.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/journalists/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search Journalists](https://docs.perigon.io/docs/journalist-data)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | — |
| `id` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `name` | query | `string` | no | — |
| `twitter` | query | `string` | no | — |
| `page` | query | `number` | no | — |
| `size` | query | `number` | no | — |
| `source` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `topic` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `category` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `label` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `minMonthlyPosts` | query | `number` | no | — |
| `maxMonthlyPosts` | query | `number` | no | — |
| `country` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `updatedAtFrom` | query | `date` | no | — |
| `updatedAtTo` | query | `date` | no | — |
| `showNumResults` | query | `boolean` | no | — |
