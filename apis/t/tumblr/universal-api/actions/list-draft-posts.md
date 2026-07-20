# Tumblr: List Draft Posts

Retrieves draft posts from a Tumblr blog.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-draft-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-draft-posts?connectionId=$CONNECTION_ID&blogIdentifier=mindcloudapps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "mindcloudapps"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-draft-posts?${params}`, {
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
| `blogIdentifier` | string | yes | Any Tumblr blog identifier for the target blog. Example: `mindcloudapps`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beforeId` | string | no | Return draft posts that appear before this post ID. Example: `1772822948`. |
| `filter` | list<string> | no | Format to return instead of default HTML output. One of: `raw`, `text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "posts": [
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
            "updated": 1,
            "url": "https://example.com",
            "uuid": "string"
          },
          "blogName": "Ava Chen",
          "body": "string",
          "canBlaze": true,
          "canIgnite": true,
          "canLike": true,
          "canMute": true,
          "canReblog": true,
          "canReply": true,
          "canSendInMessage": true,
          "date": "string",
          "displayAvatar": true,
          "followed": true,
          "format": "string",
          "id": 1,
          "idString": "string",
          "interactabilityBlaze": "string",
          "interactabilityReblog": "string",
          "isBlazed": true,
          "isBlazePending": true,
          "isBlocksPostFormat": true,
          "liked": true,
          "muted": true,
          "muteEndTimestamp": 1,
          "noteCount": 1,
          "parentPostUrl": "https://example.com",
          "postUrl": "https://example.com",
          "reblog": {
            "comment": "string",
            "treeHtml": "string"
          },
          "reblogDisabledReason": "string",
          "reblogKey": "string",
          "recommendedColor": {},
          "recommendedSource": {},
          "shortUrl": "https://example.com",
          "shouldOpenInLegacy": true,
          "slug": "string",
          "state": "string",
          "summary": "string",
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
| `posts[].blog.avatar[].height` | number |  |
| `posts[].blog.avatar[].url` | string |  |
| `posts[].blog.avatar[].width` | number |  |
| `posts[].blog.canShowBadges` | boolean |  |
| `posts[].blog.description` | string |  |
| `posts[].blog.name` | string |  |
| `posts[].blog.title` | string |  |
| `posts[].blog.updated` | number |  |
| `posts[].blog.url` | string |  |
| `posts[].blog.uuid` | string |  |
| `posts[].blogName` | string |  |
| `posts[].body` | string |  |
| `posts[].canBlaze` | boolean |  |
| `posts[].canIgnite` | boolean |  |
| `posts[].canLike` | boolean |  |
| `posts[].canMute` | boolean |  |
| `posts[].canReblog` | boolean |  |
| `posts[].canReply` | boolean |  |
| `posts[].canSendInMessage` | boolean |  |
| `posts[].date` | string |  |
| `posts[].displayAvatar` | boolean |  |
| `posts[].followed` | boolean |  |
| `posts[].format` | string |  |
| `posts[].id` | number |  |
| `posts[].idString` | string |  |
| `posts[].interactabilityBlaze` | string |  |
| `posts[].interactabilityReblog` | string |  |
| `posts[].isBlazed` | boolean |  |
| `posts[].isBlazePending` | boolean |  |
| `posts[].isBlocksPostFormat` | boolean |  |
| `posts[].liked` | boolean |  |
| `posts[].muted` | boolean |  |
| `posts[].muteEndTimestamp` | number |  |
| `posts[].noteCount` | number |  |
| `posts[].parentPostUrl` | string |  |
| `posts[].postUrl` | string |  |
| `posts[].reblog.comment` | string |  |
| `posts[].reblog.treeHtml` | string |  |
| `posts[].reblogDisabledReason` | string |  |
| `posts[].reblogKey` | string |  |
| `posts[].recommendedColor` | object |  |
| `posts[].recommendedSource` | object |  |
| `posts[].shortUrl` | string |  |
| `posts[].shouldOpenInLegacy` | boolean |  |
| `posts[].slug` | string |  |
| `posts[].state` | string |  |
| `posts[].summary` | string |  |
| `posts[].timestamp` | number |  |
| `posts[].title` | string |  |
| `posts[].trail[].blog.active` | boolean |  |
| `posts[].trail[].blog.canBeFollowed` | boolean |  |
| `posts[].trail[].blog.name` | string |  |
| `posts[].trail[].blog.shareFollowing` | boolean |  |
| `posts[].trail[].blog.shareLikes` | boolean |  |
| `posts[].trail[].blog.theme.avatarShape` | string |  |
| `posts[].trail[].blog.theme.backgroundColor` | string |  |
| `posts[].trail[].blog.theme.bodyFont` | string |  |
| `posts[].trail[].blog.theme.headerBounds` | string |  |
| `posts[].trail[].blog.theme.headerImage` | string |  |
| `posts[].trail[].blog.theme.headerImageFocused` | string |  |
| `posts[].trail[].blog.theme.headerImagePoster` | string |  |
| `posts[].trail[].blog.theme.headerImageScaled` | string |  |
| `posts[].trail[].blog.theme.headerStretch` | boolean |  |
| `posts[].trail[].blog.theme.linkColor` | string |  |
| `posts[].trail[].blog.theme.showAvatar` | boolean |  |
| `posts[].trail[].blog.theme.showDescription` | boolean |  |
| `posts[].trail[].blog.theme.showHeaderImage` | boolean |  |
| `posts[].trail[].blog.theme.showTitle` | boolean |  |
| `posts[].trail[].blog.theme.titleColor` | string |  |
| `posts[].trail[].blog.theme.titleFont` | string |  |
| `posts[].trail[].blog.theme.titleFontWeight` | string |  |
| `posts[].trail[].content` | string |  |
| `posts[].trail[].contentRaw` | string |  |
| `posts[].trail[].isRootItem` | boolean |  |
| `posts[].trail[].post.id` | string |  |
| `posts[].type` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/posts/draft` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-draft-posts.md) for the provider-specific parameters and requirements.

