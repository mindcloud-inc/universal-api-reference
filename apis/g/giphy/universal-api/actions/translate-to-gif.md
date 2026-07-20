# Giphy: Translate to GIF

Translates a phrase into a GIF in Giphy.

```
GET https://connect.mindcloud.co/v1/universal/giphy/latest/actions/translate-to-gif
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/translate-to-gif?connectionId=$CONNECTION_ID&s=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "s": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/translate-to-gif?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rating` | string | no |  |
| `s` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": "string",
      "analytics": {
        "onclick": {
          "url": "https://example.com"
        },
        "onload": {
          "url": "https://example.com"
        },
        "onsent": {
          "url": "https://example.com"
        }
      },
      "analyticsResponsePayload": "string",
      "bitlyGifUrl": "https://example.com",
      "bitlyUrl": "https://example.com",
      "contentUrl": "https://example.com",
      "embedUrl": "https://example.com",
      "id": "string",
      "images": {
        "downsized": {},
        "downsizedLarge": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "downsizedMedium": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "downsizedSmall": {},
        "downsizedStill": {},
        "fixedHeight": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedHeightDownsampled": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedHeightSmall": {},
        "fixedHeightSmallStill": {},
        "fixedHeightStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedWidth": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "webp": "string",
          "webpSize": "string",
          "width": "string"
        },
        "fixedWidthDownsampled": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedWidthSmall": {},
        "fixedWidthSmallStill": {},
        "fixedWidthStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "image480wStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "looping": {},
        "original": {
          "frames": "string",
          "hash": "string",
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "originalMp4": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "width": "string"
        },
        "originalStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "preview": {},
        "previewGif": {}
      },
      "importDatetime": "string",
      "isLowContrast": true,
      "isSticker": 1,
      "rating": "string",
      "slug": "string",
      "source": "string",
      "sourcePostUrl": "https://example.com",
      "sourceTld": "string",
      "title": "string",
      "trendingDatetime": "string",
      "type": "string",
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | string |  |
| `analytics` | object |  |
| `analytics.onclick` | object |  |
| `analytics.onclick.url` | string |  |
| `analytics.onload` | object |  |
| `analytics.onload.url` | string |  |
| `analytics.onsent` | object |  |
| `analytics.onsent.url` | string |  |
| `analyticsResponsePayload` | string |  |
| `bitlyGifUrl` | string |  |
| `bitlyUrl` | string |  |
| `contentUrl` | string |  |
| `embedUrl` | string |  |
| `id` | string |  |
| `images` | object |  |
| `images.downsized` | object |  |
| `images.downsizedLarge` | object |  |
| `images.downsizedLarge.height` | string |  |
| `images.downsizedLarge.size` | string |  |
| `images.downsizedLarge.url` | string |  |
| `images.downsizedLarge.width` | string |  |
| `images.downsizedMedium` | object |  |
| `images.downsizedMedium.height` | string |  |
| `images.downsizedMedium.size` | string |  |
| `images.downsizedMedium.url` | string |  |
| `images.downsizedMedium.width` | string |  |
| `images.downsizedSmall` | object |  |
| `images.downsizedStill` | object |  |
| `images.fixedHeight` | object |  |
| `images.fixedHeight.height` | string |  |
| `images.fixedHeight.size` | string |  |
| `images.fixedHeight.url` | string |  |
| `images.fixedHeight.width` | string |  |
| `images.fixedHeightDownsampled` | object |  |
| `images.fixedHeightDownsampled.height` | string |  |
| `images.fixedHeightDownsampled.size` | string |  |
| `images.fixedHeightDownsampled.url` | string |  |
| `images.fixedHeightDownsampled.width` | string |  |
| `images.fixedHeightSmall` | object |  |
| `images.fixedHeightSmallStill` | object |  |
| `images.fixedHeightStill` | object |  |
| `images.fixedHeightStill.height` | string |  |
| `images.fixedHeightStill.size` | string |  |
| `images.fixedHeightStill.url` | string |  |
| `images.fixedHeightStill.width` | string |  |
| `images.fixedWidth` | object |  |
| `images.fixedWidth.height` | string |  |
| `images.fixedWidth.size` | string |  |
| `images.fixedWidth.url` | string |  |
| `images.fixedWidth.webp` | string |  |
| `images.fixedWidth.webpSize` | string |  |
| `images.fixedWidth.width` | string |  |
| `images.fixedWidthDownsampled` | object |  |
| `images.fixedWidthDownsampled.height` | string |  |
| `images.fixedWidthDownsampled.size` | string |  |
| `images.fixedWidthDownsampled.url` | string |  |
| `images.fixedWidthDownsampled.width` | string |  |
| `images.fixedWidthSmall` | object |  |
| `images.fixedWidthSmallStill` | object |  |
| `images.fixedWidthStill` | object |  |
| `images.fixedWidthStill.height` | string |  |
| `images.fixedWidthStill.size` | string |  |
| `images.fixedWidthStill.url` | string |  |
| `images.fixedWidthStill.width` | string |  |
| `images.image480wStill` | object |  |
| `images.image480wStill.height` | string |  |
| `images.image480wStill.size` | string |  |
| `images.image480wStill.url` | string |  |
| `images.image480wStill.width` | string |  |
| `images.looping` | object |  |
| `images.original` | object |  |
| `images.original.frames` | string |  |
| `images.original.hash` | string |  |
| `images.original.height` | string |  |
| `images.original.mp4` | string |  |
| `images.original.mp4Size` | string |  |
| `images.original.size` | string |  |
| `images.original.url` | string |  |
| `images.original.width` | string |  |
| `images.originalMp4` | object |  |
| `images.originalMp4.height` | string |  |
| `images.originalMp4.mp4` | string |  |
| `images.originalMp4.mp4Size` | string |  |
| `images.originalMp4.width` | string |  |
| `images.originalStill` | object |  |
| `images.originalStill.height` | string |  |
| `images.originalStill.size` | string |  |
| `images.originalStill.url` | string |  |
| `images.originalStill.width` | string |  |
| `images.preview` | object |  |
| `images.previewGif` | object |  |
| `importDatetime` | string |  |
| `isLowContrast` | boolean |  |
| `isSticker` | number |  |
| `rating` | string |  |
| `slug` | string |  |
| `source` | string |  |
| `sourcePostUrl` | string |  |
| `sourceTld` | string |  |
| `title` | string |  |
| `trendingDatetime` | string |  |
| `type` | string |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Giphy API, this operation is `GET /v1/gifs/translate` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-to-gif.md) for the provider-specific parameters and requirements.

