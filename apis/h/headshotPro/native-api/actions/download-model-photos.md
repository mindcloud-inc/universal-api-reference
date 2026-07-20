# Download Model Photos with HeadshotPro

Retrieves download URLs for model photos from HeadshotPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/organization/models/:modelId/photos/download`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [Download Model Photos](https://www.headshotpro.com/api/photos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | ID of the model whose photos should be downloaded. |
| `photoIds` | body | `string` | no | Optional subset of photo IDs to download. Leave empty to download all photos. Send multiple values as a array. |
| `include` | body | `string` | no | URL variants to include in the download response. |
