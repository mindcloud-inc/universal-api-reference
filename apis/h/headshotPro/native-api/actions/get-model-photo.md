# Get Model Photo with HeadshotPro

Retrieves a model photo from HeadshotPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization/models/:modelId/photos/:photoId`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Get Model Photo](https://www.headshotpro.com/api/photos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | ID of the model that owns the photo. |
| `photoId` | path | `string` | yes | ID of the photo to retrieve. |
| `include` | query | `string` | no | URL variants to include: main or all. |
