# Batch Modify Filters with Control D

Updates multiple filters for a profile in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/profiles/:profileId/filters`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Batch Modify Filters](https://docs.controld.com/reference/put_profiles-profile-id-filters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Primary key (PK) of the profile |
| `filters[]` | body | `array<object>` | yes | Filters body field. |
