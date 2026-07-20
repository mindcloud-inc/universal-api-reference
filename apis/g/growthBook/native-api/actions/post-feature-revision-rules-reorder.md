# Reorder rules in an environment with GrowthBook

Reorders rules in a GrowthBook feature revision.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/rules/reorder`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Reorder rules in an environment](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `environment` | body | `string` | yes |
| `ruleIds` | body | `list<string>` | yes |
| `revisionTitle` | body | `string` | no |
| `revisionComment` | body | `string` | no |
