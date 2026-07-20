# Update Personalized Image Font Color with NiftyImages

Updates personalized image font color in NiftyImages.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Personalized`
- **Base URL:** `https://api.niftyimages.com/v1`
- **Official documentation:** [Update Personalized Image Font Color](https://api.niftyimages.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | NiftyImages image URL. |
| `FontColor` | body | `string` | yes | Font color to apply to the personalized image. |
