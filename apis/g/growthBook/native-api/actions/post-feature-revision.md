# Create a draft revision with GrowthBook

Creates a draft feature revision in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/features/:id/revisions`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Create a draft revision](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `comment` | body | `string` | no |
| `title` | body | `string` | no |
