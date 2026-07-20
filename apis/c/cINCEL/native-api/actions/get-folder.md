# Get Folder with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/folders/:folder`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Get Folder](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | UUID of the team that owns the folder. |
| `folder` | path | `string` | yes | UUID of the folder to retrieve. |
