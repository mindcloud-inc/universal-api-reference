# Update Space Settings with Pencil Spaces

## Endpoint

- **Method:** `PATCH`
- **Path:** `/spaces/:spaceId/settings/`
- **Base URL:** `https://apis.pencilapp.com/public/api`
- **Official documentation:** [Update Space Settings](https://api.pencilspaces.com/guide/spaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `settings` | body | `object` | no | Container for mutable Space settings. |
| `settings.disableAlwaysOnRecording` | body | `boolean` | no | Disable always-on recording for the Space. |
| `settings.enableWaitingRoom` | body | `boolean` | no | Enable waiting room for the Space. |
| `spaceId` | path | `string` | yes | The Pencil spaceId of the Space settings to update. |
