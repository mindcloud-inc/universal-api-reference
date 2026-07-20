# Modify Filter with Control D

Updates a filter for a profile in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId/filters/filter/:filter`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Filter](https://docs.controld.com/reference/put_profiles-profile-id-filters-filter-filter)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Primary key (PK) of the profile |
| `filter` | path | `string` | yes | Filter name |
| `status` | body | `number` | yes | Status of the filter. 1 to enable, 0 to disable. |
