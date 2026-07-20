# List Image Views with Hyperise

Retrieves image views for an image template in Hyperise.

## Endpoint

- **Method:** `GET`
- **Path:** `/image-impressions`
- **Base URL:** `https://app.hyperise.io/api/v1/regular`
- **Official documentation:** [List Image Views](https://hyperise.customerly.help/en/articles/9939-Image-Views-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | no | Optional ISO timestamp to fetch impressions since a specific time. |
| `image_hash` | query | `string` | yes | The Hyperise image template hash to fetch impressions for. |
