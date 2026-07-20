# Submit a review on a draft revision with GrowthBook

Submits a review for a GrowthBook draft revision.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/submit-review`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Submit a review on a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `comment` | body | `string` | no |
| `action` | body | `string` | no |
