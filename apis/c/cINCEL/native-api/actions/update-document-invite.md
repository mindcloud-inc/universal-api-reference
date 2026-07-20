# Update Document Invite with CINCEL

## Endpoint

- **Method:** `PATCH`
- **Path:** `/teams/:team/folders/:folder/documents/:document/invites/:invite`
- **Base URL:** `https://api.cincel.digital/v3`
- **Official documentation:** [Update Document Invite](https://docs.cincel.digital/v3/digital-signature#patch-/teams/-team-/folders/-folder-/documents/-document-/invites/-invite-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | path | `string` | yes | Team UUID from the path. |
| `folder` | path | `string` | yes | Folder UUID from the path. |
| `document` | path | `string` | yes | Document UUID from the path. |
| `invite` | path | `string` | yes | Invite UUID from the path. |
| `name` | body | `string` | no | Updated invite recipient name. |
| `email` | body | `string` | no | Updated invite recipient email. |
| `reminder_frequency` | body | `number` | no | Optional reminder interval value for the invite. |
