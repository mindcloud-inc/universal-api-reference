# Merge Users with Recombee

Merges one user into another in Recombee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:targetUserId/merge/:sourceUserId`
- **Base URL:** `https://rapi.recombee.com/{databaseId}`
- **Official documentation:** [Merge Users](https://docs.recombee.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cascadeCreate` | query | `string` | no |
| `sourceUserId` | path | `string` | yes |
| `targetUserId` | path | `string` | yes |
