# Create Activity with EARLY

Creates a new activity in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/activities`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Activity](https://developers.early.app/#21afd678-09fc-449e-974e-1734196d7124)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Activity name. |
| `color` | body | `string` | yes | Activity color in hex format. |
| `folderId` | body | `string` | yes | Folder ID that owns the activity. |
