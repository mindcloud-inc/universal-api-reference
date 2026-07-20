# Send Invite Reminder with CINCEL

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:team/folders/:folder/documents/:document/invites/:invite/notification`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Send Invite Reminder](https://docs.cincel.digital/v3/digital-signature#get-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-/notification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `folder` | path | `string` | yes | Folder UUID from the path. |
| `document` | path | `string` | yes | Document UUID from the path. |
| `invite` | path | `string` | yes | Invite UUID from the path. |
