# Create Space with Pencil Spaces

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/create`
- **Base URL:** `https://apis.pencilapp.com/public/api`
- **Official documentation:** [Create Space](https://api.pencilspaces.com/guide/spaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | no | Unique external identifier for the Space. |
| `notifyInvitees` | body | `boolean` | yes | Whether invitees should be notified when the Space is created. |
| `title` | body | `string` | no | The title of the Space. |
| `visibility` | body | `string` | no | Default visibility for the Space. |
