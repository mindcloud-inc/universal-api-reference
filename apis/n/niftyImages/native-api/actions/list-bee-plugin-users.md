# List Bee Plugin Users with NiftyImages

Retrieves Bee Plugin users from NiftyImages.

## Endpoint

- **Method:** `GET`
- **Path:** `/BeePlugin/:pluginKey/Users`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [List Bee Plugin Users](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pluginKey` | path | `string` | yes | Bee Plugin key. |
| `startDate` | query | `string` | no | Start date in ISO 8601 format. |
| `endDate` | query | `string` | no | End date in ISO 8601 format. |
