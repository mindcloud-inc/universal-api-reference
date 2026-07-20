# Create Pixel with JmpTo

Creates a pixel in JmpTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/pixel/add`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Create Pixel](https://jmpto.net/developers#create-a-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Pixel type such as gtmpixel, gapixel, fbpixel, adwordspixel, linkedinpixel, twitterpixel, adrollpixel, quorapixel, pinterest, bing, snapchat, reddit, or tiktok. |
| `name` | body | `string` | yes | Custom name for the pixel. |
| `tag` | body | `string` | yes | The tag for the pixel. |
