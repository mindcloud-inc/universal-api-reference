# List Widget Images with NiftyImages

Retrieves widget images from NiftyImages.

## Endpoint

- **Method:** `GET`
- **Path:** `/Widgets/:widgetKey/Images`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [List Widget Images](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widgetKey` | path | `string` | yes | Widget key. |
| `startDate` | query | `string` | no | Start date in ISO 8601 format. |
| `endDate` | query | `string` | no | End date in ISO 8601 format. |
