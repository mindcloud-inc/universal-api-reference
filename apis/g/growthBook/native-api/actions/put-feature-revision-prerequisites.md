# Set feature-level prerequisites in a draft revision with GrowthBook

Sets prerequisites for a GrowthBook feature revision.

## Endpoint

- **Method:** `PUT`
- **Path:** `/features/:id/revisions/:version/prerequisites`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Set feature-level prerequisites in a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `prerequisites[]` | body | `array<object>` | yes |
| `prerequisites[]` | body | `array<object>` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
