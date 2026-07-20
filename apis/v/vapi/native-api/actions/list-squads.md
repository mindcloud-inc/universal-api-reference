# List Squads with Vapi

Retrieves a list of squads from Vapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/squad`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [List Squads](https://docs.vapi.ai/api-reference/squads/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | query | `string` | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | query | `string` | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | query | `string` | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | query | `string` | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | query | `string` | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | query | `string` | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | query | `string` | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | query | `string` | no | This will return items where the updatedAt is less than or equal to the specified value. |
