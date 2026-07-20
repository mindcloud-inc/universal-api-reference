# Giphy: Search Channels

Finds channels in Giphy by search term.

```
GET https://connect.mindcloud.co/v1/universal/giphy/latest/actions/search-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giphy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giphy/latest/actions/search-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giphy/latest/actions/search-channels?${params}`, {
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
| `q` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyticsResponsePayload": "string",
      "ancestors": [
        "string"
      ],
      "bannerImage": "string",
      "contentType": "string",
      "displayName": "Ava Chen",
      "featuredGif": {
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
        "cta": {
          "link": "https://example.com",
          "text": "string"
        },
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
          "image4k": {
            "height": "string",
            "mp4": "string",
            "mp4Size": "string",
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
      "hasChildren": true,
      "id": 1,
      "isLive": true,
      "isPrivate": true,
      "isVisible": true,
      "metadataDescription": "string",
      "numChildren": 1,
      "slug": "string",
      "syncableTags": [
        "string"
      ],
      "tags": [
        "string"
      ],
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyticsResponsePayload` | string |  |
| `ancestors` | array<string> |  |
| `bannerImage` | string |  |
| `contentType` | string |  |
| `displayName` | string |  |
| `featuredGif` | object |  |
| `featuredGif.altText` | string |  |
| `featuredGif.analytics` | object |  |
| `featuredGif.analytics.onclick` | object |  |
| `featuredGif.analytics.onclick.url` | string |  |
| `featuredGif.analytics.onload` | object |  |
| `featuredGif.analytics.onload.url` | string |  |
| `featuredGif.analytics.onsent` | object |  |
| `featuredGif.analytics.onsent.url` | string |  |
| `featuredGif.analyticsResponsePayload` | string |  |
| `featuredGif.bitlyGifUrl` | string |  |
| `featuredGif.bitlyUrl` | string |  |
| `featuredGif.contentUrl` | string |  |
| `featuredGif.cta` | object |  |
| `featuredGif.cta.link` | string |  |
| `featuredGif.cta.text` | string |  |
| `featuredGif.embedUrl` | string |  |
| `featuredGif.id` | string |  |
| `featuredGif.images` | object |  |
| `featuredGif.images.downsized` | object |  |
| `featuredGif.images.downsized.height` | string |  |
| `featuredGif.images.downsized.size` | string |  |
| `featuredGif.images.downsized.url` | string |  |
| `featuredGif.images.downsized.width` | string |  |
| `featuredGif.images.downsizedLarge` | object |  |
| `featuredGif.images.downsizedLarge.height` | string |  |
| `featuredGif.images.downsizedLarge.size` | string |  |
| `featuredGif.images.downsizedLarge.url` | string |  |
| `featuredGif.images.downsizedLarge.width` | string |  |
| `featuredGif.images.downsizedMedium` | object |  |
| `featuredGif.images.downsizedMedium.height` | string |  |
| `featuredGif.images.downsizedMedium.size` | string |  |
| `featuredGif.images.downsizedMedium.url` | string |  |
| `featuredGif.images.downsizedMedium.width` | string |  |
| `featuredGif.images.downsizedSmall` | object |  |
| `featuredGif.images.downsizedSmall.height` | string |  |
| `featuredGif.images.downsizedSmall.mp4` | string |  |
| `featuredGif.images.downsizedSmall.mp4Size` | string |  |
| `featuredGif.images.downsizedSmall.width` | string |  |
| `featuredGif.images.downsizedStill` | object |  |
| `featuredGif.images.downsizedStill.height` | string |  |
| `featuredGif.images.downsizedStill.size` | string |  |
| `featuredGif.images.downsizedStill.url` | string |  |
| `featuredGif.images.downsizedStill.width` | string |  |
| `featuredGif.images.fixedHeight` | object |  |
| `featuredGif.images.fixedHeight.height` | string |  |
| `featuredGif.images.fixedHeight.mp4` | string |  |
| `featuredGif.images.fixedHeight.mp4Size` | string |  |
| `featuredGif.images.fixedHeight.size` | string |  |
| `featuredGif.images.fixedHeight.url` | string |  |
| `featuredGif.images.fixedHeight.webp` | string |  |
| `featuredGif.images.fixedHeight.webpSize` | string |  |
| `featuredGif.images.fixedHeight.width` | string |  |
| `featuredGif.images.fixedHeightDownsampled` | object |  |
| `featuredGif.images.fixedHeightDownsampled.height` | string |  |
| `featuredGif.images.fixedHeightDownsampled.size` | string |  |
| `featuredGif.images.fixedHeightDownsampled.url` | string |  |
| `featuredGif.images.fixedHeightDownsampled.webp` | string |  |
| `featuredGif.images.fixedHeightDownsampled.webpSize` | string |  |
| `featuredGif.images.fixedHeightDownsampled.width` | string |  |
| `featuredGif.images.fixedHeightSmall` | object |  |
| `featuredGif.images.fixedHeightSmall.height` | string |  |
| `featuredGif.images.fixedHeightSmall.mp4` | string |  |
| `featuredGif.images.fixedHeightSmall.mp4Size` | string |  |
| `featuredGif.images.fixedHeightSmall.size` | string |  |
| `featuredGif.images.fixedHeightSmall.url` | string |  |
| `featuredGif.images.fixedHeightSmall.webp` | string |  |
| `featuredGif.images.fixedHeightSmall.webpSize` | string |  |
| `featuredGif.images.fixedHeightSmall.width` | string |  |
| `featuredGif.images.fixedHeightSmallStill` | object |  |
| `featuredGif.images.fixedHeightSmallStill.height` | string |  |
| `featuredGif.images.fixedHeightSmallStill.size` | string |  |
| `featuredGif.images.fixedHeightSmallStill.url` | string |  |
| `featuredGif.images.fixedHeightSmallStill.width` | string |  |
| `featuredGif.images.fixedHeightStill` | object |  |
| `featuredGif.images.fixedHeightStill.height` | string |  |
| `featuredGif.images.fixedHeightStill.size` | string |  |
| `featuredGif.images.fixedHeightStill.url` | string |  |
| `featuredGif.images.fixedHeightStill.width` | string |  |
| `featuredGif.images.fixedWidth` | object |  |
| `featuredGif.images.fixedWidth.height` | string |  |
| `featuredGif.images.fixedWidth.mp4` | string |  |
| `featuredGif.images.fixedWidth.mp4Size` | string |  |
| `featuredGif.images.fixedWidth.size` | string |  |
| `featuredGif.images.fixedWidth.url` | string |  |
| `featuredGif.images.fixedWidth.webp` | string |  |
| `featuredGif.images.fixedWidth.webpSize` | string |  |
| `featuredGif.images.fixedWidth.width` | string |  |
| `featuredGif.images.fixedWidthDownsampled` | object |  |
| `featuredGif.images.fixedWidthDownsampled.height` | string |  |
| `featuredGif.images.fixedWidthDownsampled.size` | string |  |
| `featuredGif.images.fixedWidthDownsampled.url` | string |  |
| `featuredGif.images.fixedWidthDownsampled.webp` | string |  |
| `featuredGif.images.fixedWidthDownsampled.webpSize` | string |  |
| `featuredGif.images.fixedWidthDownsampled.width` | string |  |
| `featuredGif.images.fixedWidthSmall` | object |  |
| `featuredGif.images.fixedWidthSmall.height` | string |  |
| `featuredGif.images.fixedWidthSmall.mp4` | string |  |
| `featuredGif.images.fixedWidthSmall.mp4Size` | string |  |
| `featuredGif.images.fixedWidthSmall.size` | string |  |
| `featuredGif.images.fixedWidthSmall.url` | string |  |
| `featuredGif.images.fixedWidthSmall.webp` | string |  |
| `featuredGif.images.fixedWidthSmall.webpSize` | string |  |
| `featuredGif.images.fixedWidthSmall.width` | string |  |
| `featuredGif.images.fixedWidthSmallStill` | object |  |
| `featuredGif.images.fixedWidthSmallStill.height` | string |  |
| `featuredGif.images.fixedWidthSmallStill.size` | string |  |
| `featuredGif.images.fixedWidthSmallStill.url` | string |  |
| `featuredGif.images.fixedWidthSmallStill.width` | string |  |
| `featuredGif.images.fixedWidthStill` | object |  |
| `featuredGif.images.fixedWidthStill.height` | string |  |
| `featuredGif.images.fixedWidthStill.size` | string |  |
| `featuredGif.images.fixedWidthStill.url` | string |  |
| `featuredGif.images.fixedWidthStill.width` | string |  |
| `featuredGif.images.hd` | object |  |
| `featuredGif.images.hd.height` | string |  |
| `featuredGif.images.hd.mp4` | string |  |
| `featuredGif.images.hd.mp4Size` | string |  |
| `featuredGif.images.hd.width` | string |  |
| `featuredGif.images.image480wStill` | object |  |
| `featuredGif.images.image480wStill.height` | string |  |
| `featuredGif.images.image480wStill.size` | string |  |
| `featuredGif.images.image480wStill.url` | string |  |
| `featuredGif.images.image480wStill.width` | string |  |
| `featuredGif.images.image4k` | object |  |
| `featuredGif.images.image4k.height` | string |  |
| `featuredGif.images.image4k.mp4` | string |  |
| `featuredGif.images.image4k.mp4Size` | string |  |
| `featuredGif.images.image4k.width` | string |  |
| `featuredGif.images.looping` | object |  |
| `featuredGif.images.looping.height` | string |  |
| `featuredGif.images.looping.mp4` | string |  |
| `featuredGif.images.looping.mp4Size` | string |  |
| `featuredGif.images.looping.width` | string |  |
| `featuredGif.images.original` | object |  |
| `featuredGif.images.original.frames` | string |  |
| `featuredGif.images.original.hash` | string |  |
| `featuredGif.images.original.height` | string |  |
| `featuredGif.images.original.mp4` | string |  |
| `featuredGif.images.original.mp4Size` | string |  |
| `featuredGif.images.original.size` | string |  |
| `featuredGif.images.original.url` | string |  |
| `featuredGif.images.original.webp` | string |  |
| `featuredGif.images.original.webpSize` | string |  |
| `featuredGif.images.original.width` | string |  |
| `featuredGif.images.originalMp4` | object |  |
| `featuredGif.images.originalMp4.height` | string |  |
| `featuredGif.images.originalMp4.mp4` | string |  |
| `featuredGif.images.originalMp4.mp4Size` | string |  |
| `featuredGif.images.originalMp4.width` | string |  |
| `featuredGif.images.originalStill` | object |  |
| `featuredGif.images.originalStill.height` | string |  |
| `featuredGif.images.originalStill.size` | string |  |
| `featuredGif.images.originalStill.url` | string |  |
| `featuredGif.images.originalStill.width` | string |  |
| `featuredGif.images.preview` | object |  |
| `featuredGif.images.preview.height` | string |  |
| `featuredGif.images.preview.mp4` | string |  |
| `featuredGif.images.preview.mp4Size` | string |  |
| `featuredGif.images.preview.width` | string |  |
| `featuredGif.images.previewGif` | object |  |
| `featuredGif.images.previewGif.height` | string |  |
| `featuredGif.images.previewGif.size` | string |  |
| `featuredGif.images.previewGif.url` | string |  |
| `featuredGif.images.previewGif.width` | string |  |
| `featuredGif.images.previewWebp` | object |  |
| `featuredGif.images.previewWebp.height` | string |  |
| `featuredGif.images.previewWebp.size` | string |  |
| `featuredGif.images.previewWebp.url` | string |  |
| `featuredGif.images.previewWebp.width` | string |  |
| `featuredGif.importDatetime` | string |  |
| `featuredGif.isLowContrast` | boolean |  |
| `featuredGif.isSticker` | number |  |
| `featuredGif.rating` | string |  |
| `featuredGif.slug` | string |  |
| `featuredGif.source` | string |  |
| `featuredGif.sourcePostUrl` | string |  |
| `featuredGif.sourceTld` | string |  |
| `featuredGif.title` | string |  |
| `featuredGif.trendingDatetime` | string |  |
| `featuredGif.type` | string |  |
| `featuredGif.url` | string |  |
| `featuredGif.user` | object |  |
| `featuredGif.user.avatarUrl` | string |  |
| `featuredGif.user.bannerImage` | string |  |
| `featuredGif.user.bannerUrl` | string |  |
| `featuredGif.user.description` | string |  |
| `featuredGif.user.displayName` | string |  |
| `featuredGif.user.instagramUrl` | string |  |
| `featuredGif.user.isVerified` | boolean |  |
| `featuredGif.user.profileUrl` | string |  |
| `featuredGif.user.username` | string |  |
| `featuredGif.user.websiteUrl` | string |  |
| `featuredGif.username` | string |  |
| `hasChildren` | boolean |  |
| `id` | number |  |
| `isLive` | boolean |  |
| `isPrivate` | boolean |  |
| `isVisible` | boolean |  |
| `metadataDescription` | string |  |
| `numChildren` | number |  |
| `slug` | string |  |
| `syncableTags` | array<string> |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `url` | string |  |
| `user` | object |  |
| `user.avatarUrl` | string |  |
| `user.bannerImage` | string |  |
| `user.bannerUrl` | string |  |
| `user.description` | string |  |
| `user.displayName` | string |  |
| `user.instagramUrl` | string |  |
| `user.isVerified` | boolean |  |
| `user.profileUrl` | string |  |
| `user.username` | string |  |
| `user.websiteUrl` | string |  |

## Native endpoint

Through the native Giphy API, this operation is `GET /v1/channels/search` (base URL `https://api.giphy.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-channels.md) for the provider-specific parameters and requirements.

