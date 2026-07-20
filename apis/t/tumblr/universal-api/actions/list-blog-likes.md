# Tumblr: List Blog Likes

Retrieves liked posts from a Tumblr blog.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-likes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-likes?connectionId=$CONNECTION_ID&limit=25&offset=0&blogIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "blogIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-likes?${params}`, {
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
| `blogIdentifier` | string | yes | The blog whose public likes should be retrieved. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | number | no | Retrieve likes before the specified Unix timestamp. |
| `after` | number | no | Retrieve likes after the specified Unix timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "likedCount": 1,
      "likedPosts": [
        {
          "blog": {
            "avatar": [
              {
                "height": 1,
                "url": "https://example.com",
                "width": 1
              }
            ],
            "canShowBadges": true,
            "description": "string",
            "name": "Ava Chen",
            "title": "string",
            "tumblrmartAccessories": {
              "badges": [
                {
                  "destinationUrl": "https://example.com",
                  "productGroup": "string",
                  "urls": [
                    "https://example.com"
                  ]
                }
              ],
              "blueCheckmarkCount": 1
            },
            "updated": 1,
            "url": "https://example.com",
            "uuid": "string"
          },
          "blogName": "Ava Chen",
          "body": "string",
          "canBlaze": true,
          "canLike": true,
          "canReblog": true,
          "canReply": true,
          "canSendInMessage": true,
          "date": "string",
          "displayAvatar": true,
          "format": "string",
          "id": 1,
          "idString": "string",
          "interactabilityBlaze": "string",
          "interactabilityReblog": "string",
          "isBlazed": true,
          "isBlazePending": true,
          "isBlocksPostFormat": true,
          "likedTimestamp": 1,
          "noteCount": 1,
          "parentPostUrl": "https://example.com",
          "postUrl": "https://example.com",
          "reblog": {
            "comment": "string",
            "treeHtml": "string"
          },
          "reblogKey": "string",
          "recommendedColor": {},
          "recommendedSource": {},
          "shortUrl": "https://example.com",
          "shouldOpenInLegacy": true,
          "slug": "string",
          "state": "string",
          "summary": "string",
          "tags": [
            "string"
          ],
          "timestamp": 1,
          "title": "string",
          "trail": [
            {
              "blog": {
                "active": true,
                "canBeFollowed": true,
                "name": "Ava Chen",
                "shareFollowing": true,
                "shareLikes": true,
                "theme": {
                  "avatarShape": "string",
                  "backgroundColor": "string",
                  "bodyFont": "string",
                  "headerBounds": "string",
                  "headerFullHeight": 1,
                  "headerFullWidth": 1,
                  "headerImage": "string",
                  "headerImageFocused": "string",
                  "headerImagePoster": "string",
                  "headerImageScaled": "string",
                  "headerStretch": true,
                  "linkColor": "https://example.com",
                  "showAvatar": true,
                  "showDescription": true,
                  "showHeaderImage": true,
                  "showTitle": true,
                  "titleColor": "string",
                  "titleFont": "string",
                  "titleFontWeight": "string"
                }
              },
              "content": "string",
              "contentRaw": "string",
              "isRootItem": true,
              "post": {
                "id": "string"
              }
            }
          ],
          "type": "string"
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
| `likedCount` | number |  |
| `likedPosts[].blog.avatar[].height` | number |  |
| `likedPosts[].blog.avatar[].url` | string |  |
| `likedPosts[].blog.avatar[].width` | number |  |
| `likedPosts[].blog.canShowBadges` | boolean |  |
| `likedPosts[].blog.description` | string |  |
| `likedPosts[].blog.name` | string |  |
| `likedPosts[].blog.title` | string |  |
| `likedPosts[].blog.tumblrmartAccessories.badges[].destinationUrl` | string |  |
| `likedPosts[].blog.tumblrmartAccessories.badges[].productGroup` | string |  |
| `likedPosts[].blog.tumblrmartAccessories.badges[].urls[]` | string |  |
| `likedPosts[].blog.tumblrmartAccessories.blueCheckmarkCount` | number |  |
| `likedPosts[].blog.updated` | number |  |
| `likedPosts[].blog.url` | string |  |
| `likedPosts[].blog.uuid` | string |  |
| `likedPosts[].blogName` | string |  |
| `likedPosts[].body` | string |  |
| `likedPosts[].canBlaze` | boolean |  |
| `likedPosts[].canLike` | boolean |  |
| `likedPosts[].canReblog` | boolean |  |
| `likedPosts[].canReply` | boolean |  |
| `likedPosts[].canSendInMessage` | boolean |  |
| `likedPosts[].date` | string |  |
| `likedPosts[].displayAvatar` | boolean |  |
| `likedPosts[].format` | string |  |
| `likedPosts[].id` | number |  |
| `likedPosts[].idString` | string |  |
| `likedPosts[].interactabilityBlaze` | string |  |
| `likedPosts[].interactabilityReblog` | string |  |
| `likedPosts[].isBlazed` | boolean |  |
| `likedPosts[].isBlazePending` | boolean |  |
| `likedPosts[].isBlocksPostFormat` | boolean |  |
| `likedPosts[].likedTimestamp` | number |  |
| `likedPosts[].noteCount` | number |  |
| `likedPosts[].parentPostUrl` | string |  |
| `likedPosts[].postUrl` | string |  |
| `likedPosts[].reblog.comment` | string |  |
| `likedPosts[].reblog.treeHtml` | string |  |
| `likedPosts[].reblogKey` | string |  |
| `likedPosts[].recommendedColor` | object |  |
| `likedPosts[].recommendedSource` | object |  |
| `likedPosts[].shortUrl` | string |  |
| `likedPosts[].shouldOpenInLegacy` | boolean |  |
| `likedPosts[].slug` | string |  |
| `likedPosts[].state` | string |  |
| `likedPosts[].summary` | string |  |
| `likedPosts[].tags[]` | string |  |
| `likedPosts[].timestamp` | number |  |
| `likedPosts[].title` | string |  |
| `likedPosts[].trail[].blog.active` | boolean |  |
| `likedPosts[].trail[].blog.canBeFollowed` | boolean |  |
| `likedPosts[].trail[].blog.name` | string |  |
| `likedPosts[].trail[].blog.shareFollowing` | boolean |  |
| `likedPosts[].trail[].blog.shareLikes` | boolean |  |
| `likedPosts[].trail[].blog.theme.avatarShape` | string |  |
| `likedPosts[].trail[].blog.theme.backgroundColor` | string |  |
| `likedPosts[].trail[].blog.theme.bodyFont` | string |  |
| `likedPosts[].trail[].blog.theme.headerBounds` | string |  |
| `likedPosts[].trail[].blog.theme.headerFullHeight` | number |  |
| `likedPosts[].trail[].blog.theme.headerFullWidth` | number |  |
| `likedPosts[].trail[].blog.theme.headerImage` | string |  |
| `likedPosts[].trail[].blog.theme.headerImageFocused` | string |  |
| `likedPosts[].trail[].blog.theme.headerImagePoster` | string |  |
| `likedPosts[].trail[].blog.theme.headerImageScaled` | string |  |
| `likedPosts[].trail[].blog.theme.headerStretch` | boolean |  |
| `likedPosts[].trail[].blog.theme.linkColor` | string |  |
| `likedPosts[].trail[].blog.theme.showAvatar` | boolean |  |
| `likedPosts[].trail[].blog.theme.showDescription` | boolean |  |
| `likedPosts[].trail[].blog.theme.showHeaderImage` | boolean |  |
| `likedPosts[].trail[].blog.theme.showTitle` | boolean |  |
| `likedPosts[].trail[].blog.theme.titleColor` | string |  |
| `likedPosts[].trail[].blog.theme.titleFont` | string |  |
| `likedPosts[].trail[].blog.theme.titleFontWeight` | string |  |
| `likedPosts[].trail[].content` | string |  |
| `likedPosts[].trail[].contentRaw` | string |  |
| `likedPosts[].trail[].isRootItem` | boolean |  |
| `likedPosts[].trail[].post.id` | string |  |
| `likedPosts[].type` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/likes` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-blog-likes.md) for the provider-specific parameters and requirements.

