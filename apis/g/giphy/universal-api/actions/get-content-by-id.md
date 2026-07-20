# Giphy: Get Content by ID

Retrieves GIF, sticker, or clip content from Giphy by ID.

```
GET https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-content-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-content-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/get-content-by-id?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "embedUrl": "https://example.com",
      "id": "string",
      "images": {
        "downsized": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
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
        "downsizedSmall": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "width": "string"
        },
        "downsizedStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedHeight": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "size": "string",
          "url": "https://example.com",
          "webp": "string",
          "webpSize": "string",
          "width": "string"
        },
        "fixedHeightDownsampled": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "webp": "string",
          "webpSize": "string",
          "width": "string"
        },
        "fixedHeightSmall": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "size": "string",
          "url": "https://example.com",
          "webp": "string",
          "webpSize": "string",
          "width": "string"
        },
        "fixedHeightSmallStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedHeightStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedWidth": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
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
          "webp": "string",
          "webpSize": "string",
          "width": "string"
        },
        "fixedWidthSmall": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "size": "string",
          "url": "https://example.com",
          "webp": "string",
          "webpSize": "string",
          "width": "string"
        },
        "fixedWidthSmallStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "fixedWidthStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "hd": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "width": "string"
        },
        "image480wStill": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "original": {
          "frames": "string",
          "hash": "string",
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "size": "string",
          "url": "https://example.com",
          "webp": "string",
          "webpSize": "string",
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
        "preview": {
          "height": "string",
          "mp4": "string",
          "mp4Size": "string",
          "width": "string"
        },
        "previewGif": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        },
        "previewWebp": {
          "height": "string",
          "size": "string",
          "url": "https://example.com",
          "width": "string"
        }
      },
      "isLowContrast": true,
      "rating": "string",
      "source": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "user": {
        "avatarUrl": "https://example.com",
        "displayName": "Ava Chen",
        "isVerified": true,
        "profileUrl": "https://example.com",
        "username": "Ava Chen"
      },
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analytics` | object |  |
| `analytics.onclick` | object |  |
| `analytics.onclick.url` | string |  |
| `analytics.onload` | object |  |
| `analytics.onload.url` | string |  |
| `analytics.onsent` | object |  |
| `analytics.onsent.url` | string |  |
| `analyticsResponsePayload` | string |  |
| `embedUrl` | string |  |
| `id` | string |  |
| `images` | object |  |
| `images.downsized` | object |  |
| `images.downsized.height` | string |  |
| `images.downsized.size` | string |  |
| `images.downsized.url` | string |  |
| `images.downsized.width` | string |  |
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
| `images.downsizedSmall.height` | string |  |
| `images.downsizedSmall.mp4` | string |  |
| `images.downsizedSmall.mp4Size` | string |  |
| `images.downsizedSmall.width` | string |  |
| `images.downsizedStill` | object |  |
| `images.downsizedStill.height` | string |  |
| `images.downsizedStill.size` | string |  |
| `images.downsizedStill.url` | string |  |
| `images.downsizedStill.width` | string |  |
| `images.fixedHeight` | object |  |
| `images.fixedHeight.height` | string |  |
| `images.fixedHeight.mp4` | string |  |
| `images.fixedHeight.mp4Size` | string |  |
| `images.fixedHeight.size` | string |  |
| `images.fixedHeight.url` | string |  |
| `images.fixedHeight.webp` | string |  |
| `images.fixedHeight.webpSize` | string |  |
| `images.fixedHeight.width` | string |  |
| `images.fixedHeightDownsampled` | object |  |
| `images.fixedHeightDownsampled.height` | string |  |
| `images.fixedHeightDownsampled.size` | string |  |
| `images.fixedHeightDownsampled.url` | string |  |
| `images.fixedHeightDownsampled.webp` | string |  |
| `images.fixedHeightDownsampled.webpSize` | string |  |
| `images.fixedHeightDownsampled.width` | string |  |
| `images.fixedHeightSmall` | object |  |
| `images.fixedHeightSmall.height` | string |  |
| `images.fixedHeightSmall.mp4` | string |  |
| `images.fixedHeightSmall.mp4Size` | string |  |
| `images.fixedHeightSmall.size` | string |  |
| `images.fixedHeightSmall.url` | string |  |
| `images.fixedHeightSmall.webp` | string |  |
| `images.fixedHeightSmall.webpSize` | string |  |
| `images.fixedHeightSmall.width` | string |  |
| `images.fixedHeightSmallStill` | object |  |
| `images.fixedHeightSmallStill.height` | string |  |
| `images.fixedHeightSmallStill.size` | string |  |
| `images.fixedHeightSmallStill.url` | string |  |
| `images.fixedHeightSmallStill.width` | string |  |
| `images.fixedHeightStill` | object |  |
| `images.fixedHeightStill.height` | string |  |
| `images.fixedHeightStill.size` | string |  |
| `images.fixedHeightStill.url` | string |  |
| `images.fixedHeightStill.width` | string |  |
| `images.fixedWidth` | object |  |
| `images.fixedWidth.height` | string |  |
| `images.fixedWidth.mp4` | string |  |
| `images.fixedWidth.mp4Size` | string |  |
| `images.fixedWidth.size` | string |  |
| `images.fixedWidth.url` | string |  |
| `images.fixedWidth.webp` | string |  |
| `images.fixedWidth.webpSize` | string |  |
| `images.fixedWidth.width` | string |  |
| `images.fixedWidthDownsampled` | object |  |
| `images.fixedWidthDownsampled.height` | string |  |
| `images.fixedWidthDownsampled.size` | string |  |
| `images.fixedWidthDownsampled.url` | string |  |
| `images.fixedWidthDownsampled.webp` | string |  |
| `images.fixedWidthDownsampled.webpSize` | string |  |
| `images.fixedWidthDownsampled.width` | string |  |
| `images.fixedWidthSmall` | object |  |
| `images.fixedWidthSmall.height` | string |  |
| `images.fixedWidthSmall.mp4` | string |  |
| `images.fixedWidthSmall.mp4Size` | string |  |
| `images.fixedWidthSmall.size` | string |  |
| `images.fixedWidthSmall.url` | string |  |
| `images.fixedWidthSmall.webp` | string |  |
| `images.fixedWidthSmall.webpSize` | string |  |
| `images.fixedWidthSmall.width` | string |  |
| `images.fixedWidthSmallStill` | object |  |
| `images.fixedWidthSmallStill.height` | string |  |
| `images.fixedWidthSmallStill.size` | string |  |
| `images.fixedWidthSmallStill.url` | string |  |
| `images.fixedWidthSmallStill.width` | string |  |
| `images.fixedWidthStill` | object |  |
| `images.fixedWidthStill.height` | string |  |
| `images.fixedWidthStill.size` | string |  |
| `images.fixedWidthStill.url` | string |  |
| `images.fixedWidthStill.width` | string |  |
| `images.hd` | object |  |
| `images.hd.height` | string |  |
| `images.hd.mp4` | string |  |
| `images.hd.mp4Size` | string |  |
| `images.hd.width` | string |  |
| `images.image480wStill` | object |  |
| `images.image480wStill.height` | string |  |
| `images.image480wStill.size` | string |  |
| `images.image480wStill.url` | string |  |
| `images.image480wStill.width` | string |  |
| `images.original` | object |  |
| `images.original.frames` | string |  |
| `images.original.hash` | string |  |
| `images.original.height` | string |  |
| `images.original.mp4` | string |  |
| `images.original.mp4Size` | string |  |
| `images.original.size` | string |  |
| `images.original.url` | string |  |
| `images.original.webp` | string |  |
| `images.original.webpSize` | string |  |
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
| `images.preview.height` | string |  |
| `images.preview.mp4` | string |  |
| `images.preview.mp4Size` | string |  |
| `images.preview.width` | string |  |
| `images.previewGif` | object |  |
| `images.previewGif.height` | string |  |
| `images.previewGif.size` | string |  |
| `images.previewGif.url` | string |  |
| `images.previewGif.width` | string |  |
| `images.previewWebp` | object |  |
| `images.previewWebp.height` | string |  |
| `images.previewWebp.size` | string |  |
| `images.previewWebp.url` | string |  |
| `images.previewWebp.width` | string |  |
| `isLowContrast` | boolean |  |
| `rating` | string |  |
| `source` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `user` | object |  |
| `user.avatarUrl` | string |  |
| `user.displayName` | string |  |
| `user.isVerified` | boolean |  |
| `user.profileUrl` | string |  |
| `user.username` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Giphy API, this operation is `GET /v1/content/:id` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-by-id.md) for the provider-specific parameters and requirements.

