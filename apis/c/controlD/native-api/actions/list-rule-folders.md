# List Rule Folders with Control D

Retrieves rule folders for a profile from Control D.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profileId/groups`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [List Rule Folders](https://docs.controld.com/reference/get_profiles-profile-id-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Primary key (PK) of the profile |
