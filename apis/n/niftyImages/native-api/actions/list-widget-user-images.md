# List Widget User Images with NiftyImages

Retrieves widget user images from NiftyImages.

## Endpoint

- **Method:** `GET`
- **Path:** `/Widgets/:widgetKey/Images/:user`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [List Widget User Images](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widgetKey` | path | `string` | yes | Widget key. |
| `user` | path | `string` | yes | User identifier. |
| `startDate` | query | `string` | no | Start date in ISO 8601 format. |
| `endDate` | query | `string` | no | End date in ISO 8601 format. |
