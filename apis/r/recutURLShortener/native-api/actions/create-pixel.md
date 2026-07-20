# Create Pixel with Recut URL Shortener

Creates a tracking pixel in Recut URL Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/pixel/add`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Create Pixel](https://app.recut.in/developers#create-a-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `list` | yes | gtmpixel \| gapixel \| fbpixel \| adwordspixel \| linkedinpixel \| twitterpixel \| adrollpixel \| quorapixel \| pinterest \| bing \| snapchat \| reddit \| tiktok Accepted values: `0`, `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `name` | body | `string` | yes | Custom name for your pixel |
| `tag` | body | `string` | yes | The tag for the pixel |
