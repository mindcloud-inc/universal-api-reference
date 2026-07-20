# Get Favorite Model Photo with HeadshotPro

Retrieves a model's favorite photo from HeadshotPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization/models/:modelId/photos/favorite`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Get Favorite Model Photo](https://www.headshotpro.com/api/photos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | ID of the model whose favorite photo should be returned. |
