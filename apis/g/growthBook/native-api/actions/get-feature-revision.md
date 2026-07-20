# Get a single feature revision with GrowthBook

Retrieves a feature revision from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/features/:id/revisions/:version`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get a single feature revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
