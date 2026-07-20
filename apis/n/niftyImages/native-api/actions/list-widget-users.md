# List Widget Users with NiftyImages

Retrieves widget users from NiftyImages.

## Endpoint

- **Method:** `GET`
- **Path:** `/Widgets/:widgetKey/Users`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [List Widget Users](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widgetKey` | path | `string` | yes | Widget key. |
| `startDate` | query | `string` | no | Start date in ISO 8601 format. |
| `endDate` | query | `string` | no | End date in ISO 8601 format. |
