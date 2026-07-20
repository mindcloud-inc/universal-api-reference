# Search People with Perigon

Finds people in Perigon by name or Wikidata details.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Search People](https://docs.perigon.io/docs/entity-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | — |
| `wikidataId` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `occupationId` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `occupationLabel` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `page` | query | `number` | no | — |
| `size` | query | `number` | no | — |
