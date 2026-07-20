# Get Random Meme with Humor API

## Endpoint

- **Method:** `GET`
- **Path:** `/memes/random`
- **Base URL:** `https://api.humorapi.com`
- **Official documentation:** [Get Random Meme](https://humorapi.com/docs/#Random-Meme)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | query | `string` | no | Comma-separated words that must occur in the meme. |
| `keywords-in-image` | query | `boolean` | no | Whether keywords must occur in the image. |
| `media-type` | query | `string` | no | Media type, such as image, video, jpg, png, or gif. |
| `min-rating` | query | `number` | no | Minimum meme rating between 0 and 10. |
| `max-age-days` | query | `number` | no | Maximum meme age in days. |
