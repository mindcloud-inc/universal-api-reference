# Giphy: List GIF Categories

Retrieves GIF categories from Giphy.

```
GET https://connect.mindcloud.co/v1/universal/giphy/latest/actions/list-gif-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/list-gif-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/list-gif-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "gif": {
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
          "looping": {
            "height": "string",
            "mp4": "string",
            "mp4Size": "string",
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
        "user": {
          "avatarUrl": "https://example.com",
          "bannerImage": "string",
          "bannerUrl": "https://example.com",
          "description": "string",
          "displayName": "Ava Chen",
          "instagramUrl": "https://example.com",
          "isVerified": true,
          "profileUrl": "https://example.com",
          "username": "Ava Chen",
          "websiteUrl": "https://example.com"
        },
        "username": "Ava Chen"
      },
      "name": "Ava Chen",
      "nameEncoded": "Ava Chen",
      "subcategories": [
        {
          "name": "Ava Chen",
          "nameEncoded": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gif` | object |  |
| `gif.altText` | string |  |
| `gif.analytics` | object |  |
| `gif.analytics.onclick` | object |  |
| `gif.analytics.onclick.url` | string |  |
| `gif.analytics.onload` | object |  |
| `gif.analytics.onload.url` | string |  |
| `gif.analytics.onsent` | object |  |
| `gif.analytics.onsent.url` | string |  |
| `gif.analyticsResponsePayload` | string |  |
| `gif.bitlyGifUrl` | string |  |
| `gif.bitlyUrl` | string |  |
| `gif.contentUrl` | string |  |
| `gif.embedUrl` | string |  |
| `gif.id` | string |  |
| `gif.images` | object |  |
| `gif.images.downsized` | object |  |
| `gif.images.downsized.height` | string |  |
| `gif.images.downsized.size` | string |  |
| `gif.images.downsized.url` | string |  |
| `gif.images.downsized.width` | string |  |
| `gif.images.downsizedLarge` | object |  |
| `gif.images.downsizedLarge.height` | string |  |
| `gif.images.downsizedLarge.size` | string |  |
| `gif.images.downsizedLarge.url` | string |  |
| `gif.images.downsizedLarge.width` | string |  |
| `gif.images.downsizedMedium` | object |  |
| `gif.images.downsizedMedium.height` | string |  |
| `gif.images.downsizedMedium.size` | string |  |
| `gif.images.downsizedMedium.url` | string |  |
| `gif.images.downsizedMedium.width` | string |  |
| `gif.images.downsizedSmall` | object |  |
| `gif.images.downsizedSmall.height` | string |  |
| `gif.images.downsizedSmall.mp4` | string |  |
| `gif.images.downsizedSmall.mp4Size` | string |  |
| `gif.images.downsizedSmall.width` | string |  |
| `gif.images.downsizedStill` | object |  |
| `gif.images.downsizedStill.height` | string |  |
| `gif.images.downsizedStill.size` | string |  |
| `gif.images.downsizedStill.url` | string |  |
| `gif.images.downsizedStill.width` | string |  |
| `gif.images.fixedHeight` | object |  |
| `gif.images.fixedHeight.height` | string |  |
| `gif.images.fixedHeight.mp4` | string |  |
| `gif.images.fixedHeight.mp4Size` | string |  |
| `gif.images.fixedHeight.size` | string |  |
| `gif.images.fixedHeight.url` | string |  |
| `gif.images.fixedHeight.webp` | string |  |
| `gif.images.fixedHeight.webpSize` | string |  |
| `gif.images.fixedHeight.width` | string |  |
| `gif.images.fixedHeightDownsampled` | object |  |
| `gif.images.fixedHeightDownsampled.height` | string |  |
| `gif.images.fixedHeightDownsampled.size` | string |  |
| `gif.images.fixedHeightDownsampled.url` | string |  |
| `gif.images.fixedHeightDownsampled.webp` | string |  |
| `gif.images.fixedHeightDownsampled.webpSize` | string |  |
| `gif.images.fixedHeightDownsampled.width` | string |  |
| `gif.images.fixedHeightSmall` | object |  |
| `gif.images.fixedHeightSmall.height` | string |  |
| `gif.images.fixedHeightSmall.mp4` | string |  |
| `gif.images.fixedHeightSmall.mp4Size` | string |  |
| `gif.images.fixedHeightSmall.size` | string |  |
| `gif.images.fixedHeightSmall.url` | string |  |
| `gif.images.fixedHeightSmall.webp` | string |  |
| `gif.images.fixedHeightSmall.webpSize` | string |  |
| `gif.images.fixedHeightSmall.width` | string |  |
| `gif.images.fixedHeightSmallStill` | object |  |
| `gif.images.fixedHeightSmallStill.height` | string |  |
| `gif.images.fixedHeightSmallStill.size` | string |  |
| `gif.images.fixedHeightSmallStill.url` | string |  |
| `gif.images.fixedHeightSmallStill.width` | string |  |
| `gif.images.fixedHeightStill` | object |  |
| `gif.images.fixedHeightStill.height` | string |  |
| `gif.images.fixedHeightStill.size` | string |  |
| `gif.images.fixedHeightStill.url` | string |  |
| `gif.images.fixedHeightStill.width` | string |  |
| `gif.images.fixedWidth` | object |  |
| `gif.images.fixedWidth.height` | string |  |
| `gif.images.fixedWidth.mp4` | string |  |
| `gif.images.fixedWidth.mp4Size` | string |  |
| `gif.images.fixedWidth.size` | string |  |
| `gif.images.fixedWidth.url` | string |  |
| `gif.images.fixedWidth.webp` | string |  |
| `gif.images.fixedWidth.webpSize` | string |  |
| `gif.images.fixedWidth.width` | string |  |
| `gif.images.fixedWidthDownsampled` | object |  |
| `gif.images.fixedWidthDownsampled.height` | string |  |
| `gif.images.fixedWidthDownsampled.size` | string |  |
| `gif.images.fixedWidthDownsampled.url` | string |  |
| `gif.images.fixedWidthDownsampled.webp` | string |  |
| `gif.images.fixedWidthDownsampled.webpSize` | string |  |
| `gif.images.fixedWidthDownsampled.width` | string |  |
| `gif.images.fixedWidthSmall` | object |  |
| `gif.images.fixedWidthSmall.height` | string |  |
| `gif.images.fixedWidthSmall.mp4` | string |  |
| `gif.images.fixedWidthSmall.mp4Size` | string |  |
| `gif.images.fixedWidthSmall.size` | string |  |
| `gif.images.fixedWidthSmall.url` | string |  |
| `gif.images.fixedWidthSmall.webp` | string |  |
| `gif.images.fixedWidthSmall.webpSize` | string |  |
| `gif.images.fixedWidthSmall.width` | string |  |
| `gif.images.fixedWidthSmallStill` | object |  |
| `gif.images.fixedWidthSmallStill.height` | string |  |
| `gif.images.fixedWidthSmallStill.size` | string |  |
| `gif.images.fixedWidthSmallStill.url` | string |  |
| `gif.images.fixedWidthSmallStill.width` | string |  |
| `gif.images.fixedWidthStill` | object |  |
| `gif.images.fixedWidthStill.height` | string |  |
| `gif.images.fixedWidthStill.size` | string |  |
| `gif.images.fixedWidthStill.url` | string |  |
| `gif.images.fixedWidthStill.width` | string |  |
| `gif.images.hd` | object |  |
| `gif.images.hd.height` | string |  |
| `gif.images.hd.mp4` | string |  |
| `gif.images.hd.mp4Size` | string |  |
| `gif.images.hd.width` | string |  |
| `gif.images.image480wStill` | object |  |
| `gif.images.image480wStill.height` | string |  |
| `gif.images.image480wStill.size` | string |  |
| `gif.images.image480wStill.url` | string |  |
| `gif.images.image480wStill.width` | string |  |
| `gif.images.looping` | object |  |
| `gif.images.looping.height` | string |  |
| `gif.images.looping.mp4` | string |  |
| `gif.images.looping.mp4Size` | string |  |
| `gif.images.looping.width` | string |  |
| `gif.images.original` | object |  |
| `gif.images.original.frames` | string |  |
| `gif.images.original.hash` | string |  |
| `gif.images.original.height` | string |  |
| `gif.images.original.mp4` | string |  |
| `gif.images.original.mp4Size` | string |  |
| `gif.images.original.size` | string |  |
| `gif.images.original.url` | string |  |
| `gif.images.original.webp` | string |  |
| `gif.images.original.webpSize` | string |  |
| `gif.images.original.width` | string |  |
| `gif.images.originalMp4` | object |  |
| `gif.images.originalMp4.height` | string |  |
| `gif.images.originalMp4.mp4` | string |  |
| `gif.images.originalMp4.mp4Size` | string |  |
| `gif.images.originalMp4.width` | string |  |
| `gif.images.originalStill` | object |  |
| `gif.images.originalStill.height` | string |  |
| `gif.images.originalStill.size` | string |  |
| `gif.images.originalStill.url` | string |  |
| `gif.images.originalStill.width` | string |  |
| `gif.images.preview` | object |  |
| `gif.images.preview.height` | string |  |
| `gif.images.preview.mp4` | string |  |
| `gif.images.preview.mp4Size` | string |  |
| `gif.images.preview.width` | string |  |
| `gif.images.previewGif` | object |  |
| `gif.images.previewGif.height` | string |  |
| `gif.images.previewGif.size` | string |  |
| `gif.images.previewGif.url` | string |  |
| `gif.images.previewGif.width` | string |  |
| `gif.images.previewWebp` | object |  |
| `gif.images.previewWebp.height` | string |  |
| `gif.images.previewWebp.size` | string |  |
| `gif.images.previewWebp.url` | string |  |
| `gif.images.previewWebp.width` | string |  |
| `gif.importDatetime` | string |  |
| `gif.isLowContrast` | boolean |  |
| `gif.isSticker` | number |  |
| `gif.rating` | string |  |
| `gif.slug` | string |  |
| `gif.source` | string |  |
| `gif.sourcePostUrl` | string |  |
| `gif.sourceTld` | string |  |
| `gif.title` | string |  |
| `gif.trendingDatetime` | string |  |
| `gif.type` | string |  |
| `gif.url` | string |  |
| `gif.user` | object |  |
| `gif.user.avatarUrl` | string |  |
| `gif.user.bannerImage` | string |  |
| `gif.user.bannerUrl` | string |  |
| `gif.user.description` | string |  |
| `gif.user.displayName` | string |  |
| `gif.user.instagramUrl` | string |  |
| `gif.user.isVerified` | boolean |  |
| `gif.user.profileUrl` | string |  |
| `gif.user.username` | string |  |
| `gif.user.websiteUrl` | string |  |
| `gif.username` | string |  |
| `name` | string |  |
| `nameEncoded` | string |  |
| `subcategories` | array<object> |  |
| `subcategories[].name` | string |  |
| `subcategories[].nameEncoded` | string |  |

## Native endpoint

Through the native Giphy API, this operation is `GET /v1/gifs/categories` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-gif-categories.md) for the provider-specific parameters and requirements.

