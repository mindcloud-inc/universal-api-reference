# Create Document Invite with CINCEL

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:team/folders/:folder/documents/:document/invites`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Create Document Invite](https://docs.cincel.digital/v3/digital-signature#post-/teams/-team-/folders/-folder-/documents/-document-/invites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `folder` | path | `string` | yes | Folder UUID from the path. |
| `document` | path | `string` | yes | Document UUID from the path. |
| `name` | body | `string` | yes | Invitee name. |
| `email` | body | `string` | yes | Invitee email address. |
| `reminder_frequency` | body | `number` | no | Reminder frequency for the invite. |
| `type` | body | `string` | no | Invite role for the recipient. |
