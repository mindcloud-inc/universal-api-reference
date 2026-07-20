# Set Bee Plugin User Suspended with NiftyImages

Updates a Bee Plugin user suspension in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/BeePlugin/:pluginKey/Users/:user`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Set Bee Plugin User Suspended](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pluginKey` | path | `string` | yes | Bee Plugin key. |
| `user` | path | `string` | yes | User identifier. |
| `suspended` | body | `boolean` | yes | Set to true to suspend the user, or false to unsuspend the user. |
