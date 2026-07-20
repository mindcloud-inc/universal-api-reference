# List Bee Plugin User Images with NiftyImages

Retrieves Bee Plugin user images from NiftyImages.

## Endpoint

- **Method:** `GET`
- **Path:** `/BeePlugin/:pluginKey/Users/:user`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [List Bee Plugin User Images](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pluginKey` | path | `string` | yes | Bee Plugin key. |
| `user` | path | `string` | yes | User identifier. |
| `startDate` | query | `string` | no | Start date in ISO 8601 format. |
| `endDate` | query | `string` | no | End date in ISO 8601 format. |
