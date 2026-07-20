# Vector Search Articles with Perigon

Finds Perigon articles by semantic similarity to a prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/vector/news/all`
- **Base URL:** `https://api.perigon.io/v1`
- **Official documentation:** [Vector Search Articles](https://docs.perigon.io/docs/vector-endpoint)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `filter` | body | `object` | no |
| `pubDateFrom` | body | `date` | no |
| `pubDateTo` | body | `date` | no |
| `showReprints` | body | `boolean` | no |
| `size` | body | `number` | no |
| `page` | body | `number` | no |
