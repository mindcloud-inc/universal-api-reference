# List External Filters with Control D

Retrieves external filters for a profile from Control D.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profileId/filters/external`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [List External Filters](https://docs.controld.com/reference/get_profiles-profile-id-filters-external)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Primary key (PK) of the profile |
