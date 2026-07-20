# Vector Search Wikipedia with Perigon

Finds Wikipedia pages by semantic similarity through Perigon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/vector/wikipedia/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Vector Search Wikipedia](https://docs.perigon.io/docs/vector-wikipedia)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `filter` | body | `object` | no |
| `wikiRevisionFrom` | body | `date` | no |
| `wikiRevisionTo` | body | `date` | no |
| `pageviewsFrom` | body | `number` | no |
| `pageviewsTo` | body | `number` | no |
| `size` | body | `number` | no |
| `page` | body | `number` | no |
