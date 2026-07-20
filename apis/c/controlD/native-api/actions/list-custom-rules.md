# List Custom Rules with Control D

Retrieves custom rules for a profile from Control D.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profileId/rules/:folderId`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [List Custom Rules](https://docs.controld.com/reference/get_profiles-profile-id-rules-folder-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | path | `string` | yes | Primary key (PK) of the profile |
| `folderId` | path | `string` | yes | Folder ID (0 or omit for root) |
