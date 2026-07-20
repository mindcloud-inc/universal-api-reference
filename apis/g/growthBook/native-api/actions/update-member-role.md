# Update a member's global role (including any enviroment restrictions, if applicable). Can also update a member's project roles if your plan supports it. with GrowthBook

Updates a member role in GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/:id/role`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Update a member's global role (including any enviroment restrictions, if applicable). Can also update a member's project roles if your plan supports it.](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the requested resource |
| `member` | body | `object` | yes | — |
