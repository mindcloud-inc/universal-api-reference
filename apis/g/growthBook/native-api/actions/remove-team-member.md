# Remove members from team with GrowthBook

Removes members from a team in GrowthBook.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:id/members`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Remove members from team](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `members` | body | `list<string>` | yes |
