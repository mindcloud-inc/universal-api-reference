# Tumblr: List Tagged Posts

Retrieves Tumblr posts with a specific tag.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-tagged-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-tagged-posts?connectionId=$CONNECTION_ID&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-tagged-posts?${params}`, {
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
| `tag` | string | yes | The tag on the posts you'd like to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | number | no | Return posts before this timestamp. |
| `filter` | list<string> | no | Alternative post format to return. One of: `raw`, `text`. |

## Response

```json
{
  "success": true,
  "data": [
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
      "canReblog": true,
      "canReply": true,
      "canSendInMessage": true,
      "date": "string",
      "displayAvatar": true,
      "followed": true,
      "format": "string",
      "headerCta": {
        "action": {
          "action": "string",
          "meta": {
            "followTumblelogName": "Ava Chen"
          },
          "type": "string"
        },
        "label": "string"
      },
      "id": 1,
      "idString": "string",
      "interactabilityBlaze": "string",
      "interactabilityReblog": "string",
      "isBlazed": true,
      "isBlazePending": true,
      "isBlocksPostFormat": true,
      "liked": true,
      "noteCount": 1,
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
      "sourceTitle": "string",
      "sourceUrl": "https://example.com",
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
          "isCurrentItem": true,
          "isRootItem": true,
          "post": {
            "id": "string"
          }
        }
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blog.avatar[].height` | number |  |
| `blog.avatar[].url` | string |  |
| `blog.avatar[].width` | number |  |
| `blog.canShowBadges` | boolean |  |
| `blog.description` | string |  |
| `blog.name` | string |  |
| `blog.title` | string |  |
| `blog.updated` | number |  |
| `blog.url` | string |  |
| `blog.uuid` | string |  |
| `blogName` | string |  |
| `body` | string |  |
| `canBlaze` | boolean |  |
| `canIgnite` | boolean |  |
| `canLike` | boolean |  |
| `canReblog` | boolean |  |
| `canReply` | boolean |  |
| `canSendInMessage` | boolean |  |
| `date` | string |  |
| `displayAvatar` | boolean |  |
| `followed` | boolean |  |
| `format` | string |  |
| `headerCta.action.action` | string |  |
| `headerCta.action.meta.followTumblelogName` | string |  |
| `headerCta.action.type` | string |  |
| `headerCta.label` | string |  |
| `id` | number |  |
| `idString` | string |  |
| `interactabilityBlaze` | string |  |
| `interactabilityReblog` | string |  |
| `isBlazed` | boolean |  |
| `isBlazePending` | boolean |  |
| `isBlocksPostFormat` | boolean |  |
| `liked` | boolean |  |
| `noteCount` | number |  |
| `postUrl` | string |  |
| `reblog.comment` | string |  |
| `reblog.treeHtml` | string |  |
| `reblogKey` | string |  |
| `recommendedColor` | object |  |
| `recommendedSource` | object |  |
| `shortUrl` | string |  |
| `shouldOpenInLegacy` | boolean |  |
| `slug` | string |  |
| `sourceTitle` | string |  |
| `sourceUrl` | string |  |
| `state` | string |  |
| `summary` | string |  |
| `tags[]` | string |  |
| `timestamp` | number |  |
| `title` | string |  |
| `trail[].blog.active` | boolean |  |
| `trail[].blog.canBeFollowed` | boolean |  |
| `trail[].blog.name` | string |  |
| `trail[].blog.shareFollowing` | boolean |  |
| `trail[].blog.shareLikes` | boolean |  |
| `trail[].blog.theme.avatarShape` | string |  |
| `trail[].blog.theme.backgroundColor` | string |  |
| `trail[].blog.theme.bodyFont` | string |  |
| `trail[].blog.theme.headerBounds` | string |  |
| `trail[].blog.theme.headerImage` | string |  |
| `trail[].blog.theme.headerImageFocused` | string |  |
| `trail[].blog.theme.headerImagePoster` | string |  |
| `trail[].blog.theme.headerImageScaled` | string |  |
| `trail[].blog.theme.headerStretch` | boolean |  |
| `trail[].blog.theme.linkColor` | string |  |
| `trail[].blog.theme.showAvatar` | boolean |  |
| `trail[].blog.theme.showDescription` | boolean |  |
| `trail[].blog.theme.showHeaderImage` | boolean |  |
| `trail[].blog.theme.showTitle` | boolean |  |
| `trail[].blog.theme.titleColor` | string |  |
| `trail[].blog.theme.titleFont` | string |  |
| `trail[].blog.theme.titleFontWeight` | string |  |
| `trail[].content` | string |  |
| `trail[].contentRaw` | string |  |
| `trail[].isCurrentItem` | boolean |  |
| `trail[].isRootItem` | boolean |  |
| `trail[].post.id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/tagged` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tagged-posts.md) for the provider-specific parameters and requirements.

