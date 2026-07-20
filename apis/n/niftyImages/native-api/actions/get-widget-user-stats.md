# Get Widget User Stats with NiftyImages

Retrieves widget user stats from NiftyImages.

## Endpoint

- **Method:** `GET`
- **Path:** `/Widgets/:widgetKey/Users/:user`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Get Widget User Stats](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widgetKey` | path | `string` | yes | Widget key. |
| `user` | path | `string` | yes | User identifier. |
| `startDate` | query | `string` | no | Start date in ISO 8601 format. |
| `endDate` | query | `string` | no | End date in ISO 8601 format. |
