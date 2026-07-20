# Update Folder with CINCEL

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/:team/folders/:folder`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Update Folder](https://docs.cincel.digital/v3/digital-signature#patch-/teams/-team-/folders/-folder-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | UUID of the team that owns the folder. |
| `folder` | path | `string` | yes | UUID of the folder to update. |
| `name` | body | `string` | no | Updated folder name. |
| `team` | body | `string` | no | Owning team UUID in the request body when required by the provider. |
