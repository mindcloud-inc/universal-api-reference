# Delete Folder with CINCEL

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:team/folders/:folder`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Delete Folder](https://docs.cincel.digital/v3/digital-signature#delete-/teams/-team-/folders/-folder-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | UUID of the team that owns the folder. |
| `folder` | path | `string` | yes | UUID of the folder to delete. |
