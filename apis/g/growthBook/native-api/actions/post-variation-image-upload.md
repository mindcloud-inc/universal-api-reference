# Upload a variation screenshot with GrowthBook

Uploads a variation screenshot to GrowthBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/experiments/:id/variation/:variationId/screenshot/upload`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Upload a variation screenshot](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `variationId` | path | `string` | yes | — |
| `screenshot` | body | `string` | yes | Base64-encoded screenshot data |
| `contentType` | body | `string` | yes | MIME type of the screenshot |
| `description` | body | `string` | no | Optional description for the screenshot |
