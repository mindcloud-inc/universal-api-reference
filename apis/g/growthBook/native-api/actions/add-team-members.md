# Add members to team with GrowthBook

Adds members to a team in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:id/members`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Add members to team](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `members` | body | `list<string>` | yes |
