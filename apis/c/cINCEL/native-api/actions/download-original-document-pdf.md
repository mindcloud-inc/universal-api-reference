# Download Original Document PDF with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/folders/:folder/documents/:document.pdf`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Download Original Document PDF](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `folder` | path | `string` | yes | Folder UUID from the path. |
| `document` | path | `string` | yes | Document UUID from the path. |
