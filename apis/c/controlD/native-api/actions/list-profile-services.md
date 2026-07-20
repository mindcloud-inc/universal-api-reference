# List Profile Services with Control D

Retrieves services for a profile from Control D.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profileId/services`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [List Profile Services](https://docs.controld.com/reference/get_profiles-profile-id-services)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Primary key (PK) of the profile |
