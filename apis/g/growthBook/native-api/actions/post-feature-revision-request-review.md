# Request review for a draft revision with GrowthBook

Requests review for a GrowthBook draft revision.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/request-review`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Request review for a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `comment` | body | `string` | no |
