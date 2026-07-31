# Caption Image with Imgflip

## Endpoint

- **Method:** `POST`
- **Path:** `/caption_image`
- **Base URL:** `https://api.imgflip.com`
- **Official documentation:** [Caption Image](https://imgflip.com/api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | Template ID returned by List Popular Memes. |
| `text0` | body | `string` | yes | Top caption text. Do not use with boxes. |
| `text1` | body | `string` | yes | Bottom caption text. Do not use with boxes. |
| `font` | body | `string` | no | Optional font family. Imgflip defaults to impact. |
| `max_font_size` | body | `number` | no | Optional maximum font size in pixels. Imgflip defaults to 50. |
