# Rebase a draft revision onto the current live version with GrowthBook

Rebases a draft feature revision in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions/:version/rebase`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Rebase a draft revision onto the current live version](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `version` | path | `number` | yes |
| `conflictResolutions` | body | `object` | no |
