# Discard a draft revision with GrowthBook

Discards a draft feature revision in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/discard`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Discard a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
