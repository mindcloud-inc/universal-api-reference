# Update Personalized Image Text with NiftyImages

Updates personalized image text in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Personalized`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Personalized Image Text](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages image URL. |
| `ImageText` | body | `string` | yes | Text to render on the image. |
| `DefaultText` | body | `string` | no | Fallback text for the personalized image. |
