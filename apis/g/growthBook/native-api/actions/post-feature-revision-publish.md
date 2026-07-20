# Publish a draft revision with GrowthBook

Publishes a draft feature revision in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/publish`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Publish a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `comment` | body | `string` | no |
