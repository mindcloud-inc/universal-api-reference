# Delete Document Invite with CINCEL

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:team/folders/:folder/documents/:document/invites/:invite`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Delete Document Invite](https://docs.cincel.digital/v3/digital-signature#delete-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `folder` | path | `string` | yes | Folder UUID from the path. |
| `document` | path | `string` | yes | Document UUID from the path. |
| `invite` | path | `string` | yes | Invite UUID from the path. |
