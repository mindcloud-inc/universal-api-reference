# Delete a single team with GrowthBook

Deletes an existing team from GrowthBook.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:id`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Delete a single team](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `deleteMembers` | query | `string` | no | When 'true', enables deleting a team that contains members |
