# Create Folder with CINCEL

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:team/folders`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Create Folder](https://docs.cincel.digital/v3/digital-signature#post-/teams/-team-/folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | UUID of the team that will own the folder. |
| `name` | body | `string` | yes | Name of the folder to create. |
