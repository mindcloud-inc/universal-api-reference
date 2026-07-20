# Revert the feature to a prior revision with GrowthBook

Reverts a GrowthBook feature to a prior revision.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/revert`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Revert the feature to a prior revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `strategy` | body | `string` | no |
| `comment` | body | `string` | no |
| `title` | body | `string` | no |
