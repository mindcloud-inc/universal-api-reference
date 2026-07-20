# Set Widget User Suspended with NiftyImages

Updates a widget user suspension in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Widgets/:widgetKey/Users/:user`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Set Widget User Suspended](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widgetKey` | path | `string` | yes | Widget key. |
| `user` | path | `string` | yes | User identifier. |
| `suspended` | body | `boolean` | yes | Set to true to suspend the user, or false to unsuspend the user. |
