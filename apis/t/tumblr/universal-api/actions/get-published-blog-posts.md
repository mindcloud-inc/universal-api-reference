# Tumblr: Get Published Blog Posts

Retrieves published posts from a Tumblr blog.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-published-blog-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-published-blog-posts?connectionId=$CONNECTION_ID&limit=25&offset=0&blogIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "blogIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/get-published-blog-posts?${params}`, {
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
| `blogIdentifier` | string | yes | Any blog identifier. |
| `type` | list<string> | no | Post type to return. One of: `answer`, `audio`, `chat`, `link`, `photo`, `quote`, `text`, `video`. |
| `tag` | string | no | Limit the response to posts with the specified tag. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Return a specific post ID. |
| `reblogInfo` | boolean | no | Return reblog information. |
| `notesInfo` | boolean | no | Return note count and note metadata. |
| `filter` | list<string> | no | Alternative post format to return. One of: `raw`, `text`. |
| `before` | number | no | Return posts published before this Unix timestamp in seconds. |
| `after` | number | no | Return posts published after this Unix timestamp in seconds. |
| `sort` | list<string> | no | Sort order for the returned posts. One of: `asc`, `desc`. Default: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blog": {
        "admin": true,
        "ask": true,
        "askAnon": true,
        "askPageTitle": "string",
        "asksAllowMedia": true,
        "avatar": [
          {
            "height": 1,
            "url": "https://example.com",
            "width": 1
          }
        ],
        "canChat": true,
        "canSendFanMail": true,
        "canSubscribe": true,
        "description": "string",
        "drafts": 1,
        "facebook": "string",
        "facebookOpengraphEnabled": "string",
        "followed": true,
        "followers": 1,
        "isBlockedFromPrimary": true,
        "isNsfw": true,
        "likes": 1,
        "messages": 1,
        "name": "Ava Chen",
        "posts": 1,
        "primary": true,
        "queue": 1,
        "shareLikes": true,
        "subscribed": true,
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
        },
        "themeId": 1,
        "title": "string",
        "totalPosts": 1,
        "tweet": "string",
        "twitterEnabled": true,
        "twitterSend": true,
        "type": "string",
        "updated": 1,
        "url": "https://example.com",
        "uuid": "string"
      },
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
          "canBlaze": true,
          "canIgnite": true,
          "canLike": true,
          "canMute": true,
          "canReblog": true,
          "canReply": true,
          "canSendInMessage": true,
          "content": [
            {
              "subtype": "string",
              "text": "string",
              "type": "string"
            }
          ],
          "date": "string",
          "displayAvatar": true,
          "followed": true,
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
          "originalType": "string",
          "postUrl": "https://example.com",
          "reblogKey": "string",
          "recommendedColor": {},
          "recommendedSource": {},
          "shortUrl": "https://example.com",
          "shouldOpenInLegacy": true,
          "slug": "string",
          "state": "string",
          "summary": "string",
          "timestamp": 1,
          "type": "string"
        }
      ],
      "totalPosts": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blog.admin` | boolean |  |
| `blog.ask` | boolean |  |
| `blog.askAnon` | boolean |  |
| `blog.askPageTitle` | string |  |
| `blog.asksAllowMedia` | boolean |  |
| `blog.avatar[].height` | number |  |
| `blog.avatar[].url` | string |  |
| `blog.avatar[].width` | number |  |
| `blog.canChat` | boolean |  |
| `blog.canSendFanMail` | boolean |  |
| `blog.canSubscribe` | boolean |  |
| `blog.description` | string |  |
| `blog.drafts` | number |  |
| `blog.facebook` | string |  |
| `blog.facebookOpengraphEnabled` | string |  |
| `blog.followed` | boolean |  |
| `blog.followers` | number |  |
| `blog.isBlockedFromPrimary` | boolean |  |
| `blog.isNsfw` | boolean |  |
| `blog.likes` | number |  |
| `blog.messages` | number |  |
| `blog.name` | string |  |
| `blog.posts` | number |  |
| `blog.primary` | boolean |  |
| `blog.queue` | number |  |
| `blog.shareLikes` | boolean |  |
| `blog.subscribed` | boolean |  |
| `blog.theme.avatarShape` | string |  |
| `blog.theme.backgroundColor` | string |  |
| `blog.theme.bodyFont` | string |  |
| `blog.theme.headerBounds` | string |  |
| `blog.theme.headerImage` | string |  |
| `blog.theme.headerImageFocused` | string |  |
| `blog.theme.headerImagePoster` | string |  |
| `blog.theme.headerImageScaled` | string |  |
| `blog.theme.headerStretch` | boolean |  |
| `blog.theme.linkColor` | string |  |
| `blog.theme.showAvatar` | boolean |  |
| `blog.theme.showDescription` | boolean |  |
| `blog.theme.showHeaderImage` | boolean |  |
| `blog.theme.showTitle` | boolean |  |
| `blog.theme.titleColor` | string |  |
| `blog.theme.titleFont` | string |  |
| `blog.theme.titleFontWeight` | string |  |
| `blog.themeId` | number |  |
| `blog.title` | string |  |
| `blog.totalPosts` | number |  |
| `blog.tweet` | string |  |
| `blog.twitterEnabled` | boolean |  |
| `blog.twitterSend` | boolean |  |
| `blog.type` | string |  |
| `blog.updated` | number |  |
| `blog.url` | string |  |
| `blog.uuid` | string |  |
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
| `posts[].canBlaze` | boolean |  |
| `posts[].canIgnite` | boolean |  |
| `posts[].canLike` | boolean |  |
| `posts[].canMute` | boolean |  |
| `posts[].canReblog` | boolean |  |
| `posts[].canReply` | boolean |  |
| `posts[].canSendInMessage` | boolean |  |
| `posts[].content[].subtype` | string |  |
| `posts[].content[].text` | string |  |
| `posts[].content[].type` | string |  |
| `posts[].date` | string |  |
| `posts[].displayAvatar` | boolean |  |
| `posts[].followed` | boolean |  |
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
| `posts[].originalType` | string |  |
| `posts[].postUrl` | string |  |
| `posts[].reblogKey` | string |  |
| `posts[].recommendedColor` | object |  |
| `posts[].recommendedSource` | object |  |
| `posts[].shortUrl` | string |  |
| `posts[].shouldOpenInLegacy` | boolean |  |
| `posts[].slug` | string |  |
| `posts[].state` | string |  |
| `posts[].summary` | string |  |
| `posts[].timestamp` | number |  |
| `posts[].type` | string |  |
| `totalPosts` | number |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/posts` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-published-blog-posts.md) for the provider-specific parameters and requirements.

